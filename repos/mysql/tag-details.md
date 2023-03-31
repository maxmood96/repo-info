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
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
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
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
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
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32`

```console
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
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
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
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
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:a5410720a5235965f600a6a75779bcb619d57e77149453f2ae628676a4174ef7
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
$ docker pull mysql@sha256:2cb5e59c2166e94a3fb7e4da239e09112097af483f9f2bc8f1f87e3394fdf533
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155469964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf06b16ec818518626ff3ed5da8c0225355d4c65b22bdfc40101de31283a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 31 Mar 2023 21:40:18 GMT
ADD file:c201d04749a3d092a7936542e4e280194ac00d3a3f3e3cd1722455429b0c4d18 in / 
# Fri, 31 Mar 2023 21:40:19 GMT
CMD ["/bin/bash"]
# Fri, 31 Mar 2023 22:04:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Fri, 31 Mar 2023 22:04:22 GMT
ENV GOSU_VERSION=1.16
# Fri, 31 Mar 2023 22:04:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Fri, 31 Mar 2023 22:04:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Fri, 31 Mar 2023 22:04:52 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 31 Mar 2023 22:04:52 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:04:53 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Fri, 31 Mar 2023 22:05:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Fri, 31 Mar 2023 22:05:23 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Fri, 31 Mar 2023 22:05:23 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Fri, 31 Mar 2023 22:05:56 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Fri, 31 Mar 2023 22:05:58 GMT
VOLUME [/var/lib/mysql]
# Fri, 31 Mar 2023 22:05:58 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Fri, 31 Mar 2023 22:05:58 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Fri, 31 Mar 2023 22:05:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 22:05:58 GMT
EXPOSE 3306 33060
# Fri, 31 Mar 2023 22:05:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e83b78392ad9185bc4dcd144ceb39aea57035dc1457949ceaa1ac05c786aeaab`  
		Last Modified: Fri, 31 Mar 2023 21:41:31 GMT  
		Size: 43.5 MB (43477120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0a198b4661e7137950107d93cc0d1d1683997075fbe25fa15bfd4fe4872d23`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b64caa1d1176052f133a648c0ccdac9d58820eaecc93dcafed3037c272f69f48`  
		Last Modified: Fri, 31 Mar 2023 22:06:25 GMT  
		Size: 913.0 KB (912994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b623725aef61ae271eebbaaa097ef8dccac6137d9e501e6a76b7268200a079`  
		Last Modified: Fri, 31 Mar 2023 22:06:24 GMT  
		Size: 4.5 MB (4465645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc28d9dffb0bc2ec2dee7217b4f7309e9a725e03fbe2cb964eb7ee315e9b953`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 2.6 KB (2629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc25ff09cf7ae8d493a952da14c6fa4d5007931837e95d4812f16f993b04c31b`  
		Last Modified: Fri, 31 Mar 2023 22:06:23 GMT  
		Size: 337.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90e5cc99a8927613d5dee2323f54b9e51b7f2bc12c4db5f3e4ad2b5f8ff72c63`  
		Last Modified: Fri, 31 Mar 2023 22:06:27 GMT  
		Size: 55.6 MB (55605496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3e21b4b04614edda91cee3ad4c4e68e424716d2475c3ffc8b895084fdf8ef1`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e36898bc62c6112837a45eac0f045e5d135444cad6693bb1f533c8a5251b4b`  
		Last Modified: Fri, 31 Mar 2023 22:06:28 GMT  
		Size: 51.0 MB (50999027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f2c27ee8e612061906361bf78f27724a63c8d02272088455e641359abe66cd`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe8af54c051071611505039a849148de5d773ebdd75d058d75f7c7856fb3a30`  
		Last Modified: Fri, 31 Mar 2023 22:06:21 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
