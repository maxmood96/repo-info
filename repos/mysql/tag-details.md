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
$ docker pull mysql@sha256:b3a86578a582617214477d91e47e850f9e18df0b5d1644fb2d96d91a340b8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:5ecf646122c4fcbda81983c9e93e81a011b0593c9c19fbfc55b48bd1c23bc790
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147495b3a5ce957dee2319099a8808c1418e0b0a2c82c9b2396c5fb4b688509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:46:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:46:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:46:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:46:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 13 Jul 2022 06:46:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:46:49 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 26 Jul 2022 23:28:50 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Tue, 26 Jul 2022 23:28:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:29:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:29:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:29:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Tue, 26 Jul 2022 23:29:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:29:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:29:32 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:29:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:29:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:29:33 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:29:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ccd63cdb4ccb21c25d292be05bf37ee54a40a0746acdfa962a45a29a08b51`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f28a94c51f0d4090e9d6792e3ac48d318cc96056520dd0d7f6e6d2db851891`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 930.2 KB (930231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feea2a503b5e8b906b70f33abda7cc47dd30cb72363f804838831a48fdc8a74`  
		Last Modified: Wed, 13 Jul 2022 06:48:49 GMT  
		Size: 4.5 MB (4549473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd5852ecd934862db097d1380b3c2fe6471908610bbc2ac0b10f3daf59a183`  
		Last Modified: Wed, 13 Jul 2022 06:48:47 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5c3b24fd570d47fbe75cbe51b9f8428d58446368bf07022c42c52d943a9bb`  
		Last Modified: Tue, 26 Jul 2022 23:31:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a546386a618f1071083b0d9d357cceff83aa39db239224f71a97968e35fff2`  
		Last Modified: Tue, 26 Jul 2022 23:31:43 GMT  
		Size: 25.5 MB (25512706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b18297cf83f401e9641ba48cc9948ea3593821b42cae5990bacffd230c5ae5`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f23335fb87ecace32a157428c706c308e2b71a97f9038204e208cf838bea6`  
		Last Modified: Tue, 26 Jul 2022 23:31:48 GMT  
		Size: 48.6 MB (48608834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4171261fac245494f48f61a9a3392736658b7c31f707783b796d952008ebb`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dcc6c8de93eee9106fbbff2915b00236e56b1bf820f724d87daae33cb57e8d`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:8a2b6cea84dbac03339b72c39f0ac5be07816ad26e7f00ed2b1f13cba01512f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fea7de9666bd9c9afeb553ffc38f359372dcb5ceef2d93616dcd5d8d54aa2823
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162536048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93726b1fb68c052d2b8d15ec32edca75015c2b448a10acce6a4dacbce95a3fb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:58 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:50:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:50:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:50:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:50:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 02 Aug 2022 04:50:14 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Tue, 02 Aug 2022 04:50:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:50:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:50:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:50:34 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:50:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:50:35 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:50:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dde536a29c092d40250b981fea24b05a9dc01fae8ed7473b95bc09a7919e3d4`  
		Last Modified: Tue, 02 Aug 2022 04:51:46 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6dbe684fb4d5f85516eab17e234538e624294dc9802813fe7d5471d7f0fb22`  
		Last Modified: Tue, 02 Aug 2022 04:51:45 GMT  
		Size: 4.2 MB (4179188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e7b9b4c2f95f52a2e335c627e253309b4990e6aa70126b87f466b03ead54a6`  
		Last Modified: Tue, 02 Aug 2022 04:51:44 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a63e201542d8ec3a607182805f0550389619da1b31e6b5565635bc9894dfb8`  
		Last Modified: Tue, 02 Aug 2022 04:51:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6f168d24831f4c6e191421ef112b0fd55a6bdf1e335246a8e3e6848d150c84`  
		Last Modified: Tue, 02 Aug 2022 04:51:47 GMT  
		Size: 14.1 MB (14087033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8f214492792e72d7b500c0a1e8e5df55d26bb07aa7c919911c04f1a9e7c1f2`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d2966183c1fe326b26d0309659babda5141268f4e55ce8016cef16b6bcfc1`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294ee13b3a068f95d69addf91bb1ee6e73c9cb2b69798cdcf73ffa4be99e0cda`  
		Last Modified: Tue, 02 Aug 2022 04:51:57 GMT  
		Size: 115.7 MB (115733135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412f4ed71e26e9a985d22750ab20a1a75d135bf32ece0b1c58093fb9407a814`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c9e63111cdb7e0c20a5b1cedfc5aec938f7eb9239d98209c8d34f2aa4000a`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:b3a86578a582617214477d91e47e850f9e18df0b5d1644fb2d96d91a340b8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ecf646122c4fcbda81983c9e93e81a011b0593c9c19fbfc55b48bd1c23bc790
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147495b3a5ce957dee2319099a8808c1418e0b0a2c82c9b2396c5fb4b688509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:46:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:46:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:46:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:46:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 13 Jul 2022 06:46:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:46:49 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 26 Jul 2022 23:28:50 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Tue, 26 Jul 2022 23:28:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:29:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:29:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:29:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Tue, 26 Jul 2022 23:29:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:29:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:29:32 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:29:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:29:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:29:33 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:29:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ccd63cdb4ccb21c25d292be05bf37ee54a40a0746acdfa962a45a29a08b51`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f28a94c51f0d4090e9d6792e3ac48d318cc96056520dd0d7f6e6d2db851891`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 930.2 KB (930231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feea2a503b5e8b906b70f33abda7cc47dd30cb72363f804838831a48fdc8a74`  
		Last Modified: Wed, 13 Jul 2022 06:48:49 GMT  
		Size: 4.5 MB (4549473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd5852ecd934862db097d1380b3c2fe6471908610bbc2ac0b10f3daf59a183`  
		Last Modified: Wed, 13 Jul 2022 06:48:47 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5c3b24fd570d47fbe75cbe51b9f8428d58446368bf07022c42c52d943a9bb`  
		Last Modified: Tue, 26 Jul 2022 23:31:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a546386a618f1071083b0d9d357cceff83aa39db239224f71a97968e35fff2`  
		Last Modified: Tue, 26 Jul 2022 23:31:43 GMT  
		Size: 25.5 MB (25512706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b18297cf83f401e9641ba48cc9948ea3593821b42cae5990bacffd230c5ae5`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f23335fb87ecace32a157428c706c308e2b71a97f9038204e208cf838bea6`  
		Last Modified: Tue, 26 Jul 2022 23:31:48 GMT  
		Size: 48.6 MB (48608834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4171261fac245494f48f61a9a3392736658b7c31f707783b796d952008ebb`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dcc6c8de93eee9106fbbff2915b00236e56b1bf820f724d87daae33cb57e8d`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:b3a86578a582617214477d91e47e850f9e18df0b5d1644fb2d96d91a340b8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:5ecf646122c4fcbda81983c9e93e81a011b0593c9c19fbfc55b48bd1c23bc790
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147495b3a5ce957dee2319099a8808c1418e0b0a2c82c9b2396c5fb4b688509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:46:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:46:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:46:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:46:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 13 Jul 2022 06:46:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:46:49 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 26 Jul 2022 23:28:50 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Tue, 26 Jul 2022 23:28:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:29:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:29:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:29:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Tue, 26 Jul 2022 23:29:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:29:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:29:32 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:29:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:29:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:29:33 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:29:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ccd63cdb4ccb21c25d292be05bf37ee54a40a0746acdfa962a45a29a08b51`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f28a94c51f0d4090e9d6792e3ac48d318cc96056520dd0d7f6e6d2db851891`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 930.2 KB (930231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feea2a503b5e8b906b70f33abda7cc47dd30cb72363f804838831a48fdc8a74`  
		Last Modified: Wed, 13 Jul 2022 06:48:49 GMT  
		Size: 4.5 MB (4549473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd5852ecd934862db097d1380b3c2fe6471908610bbc2ac0b10f3daf59a183`  
		Last Modified: Wed, 13 Jul 2022 06:48:47 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5c3b24fd570d47fbe75cbe51b9f8428d58446368bf07022c42c52d943a9bb`  
		Last Modified: Tue, 26 Jul 2022 23:31:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a546386a618f1071083b0d9d357cceff83aa39db239224f71a97968e35fff2`  
		Last Modified: Tue, 26 Jul 2022 23:31:43 GMT  
		Size: 25.5 MB (25512706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b18297cf83f401e9641ba48cc9948ea3593821b42cae5990bacffd230c5ae5`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f23335fb87ecace32a157428c706c308e2b71a97f9038204e208cf838bea6`  
		Last Modified: Tue, 26 Jul 2022 23:31:48 GMT  
		Size: 48.6 MB (48608834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4171261fac245494f48f61a9a3392736658b7c31f707783b796d952008ebb`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dcc6c8de93eee9106fbbff2915b00236e56b1bf820f724d87daae33cb57e8d`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:8a2b6cea84dbac03339b72c39f0ac5be07816ad26e7f00ed2b1f13cba01512f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fea7de9666bd9c9afeb553ffc38f359372dcb5ceef2d93616dcd5d8d54aa2823
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162536048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93726b1fb68c052d2b8d15ec32edca75015c2b448a10acce6a4dacbce95a3fb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:58 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:50:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:50:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:50:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:50:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 02 Aug 2022 04:50:14 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Tue, 02 Aug 2022 04:50:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:50:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:50:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:50:34 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:50:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:50:35 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:50:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dde536a29c092d40250b981fea24b05a9dc01fae8ed7473b95bc09a7919e3d4`  
		Last Modified: Tue, 02 Aug 2022 04:51:46 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6dbe684fb4d5f85516eab17e234538e624294dc9802813fe7d5471d7f0fb22`  
		Last Modified: Tue, 02 Aug 2022 04:51:45 GMT  
		Size: 4.2 MB (4179188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e7b9b4c2f95f52a2e335c627e253309b4990e6aa70126b87f466b03ead54a6`  
		Last Modified: Tue, 02 Aug 2022 04:51:44 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a63e201542d8ec3a607182805f0550389619da1b31e6b5565635bc9894dfb8`  
		Last Modified: Tue, 02 Aug 2022 04:51:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6f168d24831f4c6e191421ef112b0fd55a6bdf1e335246a8e3e6848d150c84`  
		Last Modified: Tue, 02 Aug 2022 04:51:47 GMT  
		Size: 14.1 MB (14087033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8f214492792e72d7b500c0a1e8e5df55d26bb07aa7c919911c04f1a9e7c1f2`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d2966183c1fe326b26d0309659babda5141268f4e55ce8016cef16b6bcfc1`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294ee13b3a068f95d69addf91bb1ee6e73c9cb2b69798cdcf73ffa4be99e0cda`  
		Last Modified: Tue, 02 Aug 2022 04:51:57 GMT  
		Size: 115.7 MB (115733135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412f4ed71e26e9a985d22750ab20a1a75d135bf32ece0b1c58093fb9407a814`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c9e63111cdb7e0c20a5b1cedfc5aec938f7eb9239d98209c8d34f2aa4000a`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:b3a86578a582617214477d91e47e850f9e18df0b5d1644fb2d96d91a340b8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ecf646122c4fcbda81983c9e93e81a011b0593c9c19fbfc55b48bd1c23bc790
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147495b3a5ce957dee2319099a8808c1418e0b0a2c82c9b2396c5fb4b688509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:46:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:46:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:46:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:46:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 13 Jul 2022 06:46:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:46:49 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 26 Jul 2022 23:28:50 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Tue, 26 Jul 2022 23:28:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:29:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:29:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:29:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Tue, 26 Jul 2022 23:29:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:29:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:29:32 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:29:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:29:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:29:33 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:29:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ccd63cdb4ccb21c25d292be05bf37ee54a40a0746acdfa962a45a29a08b51`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f28a94c51f0d4090e9d6792e3ac48d318cc96056520dd0d7f6e6d2db851891`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 930.2 KB (930231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feea2a503b5e8b906b70f33abda7cc47dd30cb72363f804838831a48fdc8a74`  
		Last Modified: Wed, 13 Jul 2022 06:48:49 GMT  
		Size: 4.5 MB (4549473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd5852ecd934862db097d1380b3c2fe6471908610bbc2ac0b10f3daf59a183`  
		Last Modified: Wed, 13 Jul 2022 06:48:47 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5c3b24fd570d47fbe75cbe51b9f8428d58446368bf07022c42c52d943a9bb`  
		Last Modified: Tue, 26 Jul 2022 23:31:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a546386a618f1071083b0d9d357cceff83aa39db239224f71a97968e35fff2`  
		Last Modified: Tue, 26 Jul 2022 23:31:43 GMT  
		Size: 25.5 MB (25512706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b18297cf83f401e9641ba48cc9948ea3593821b42cae5990bacffd230c5ae5`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f23335fb87ecace32a157428c706c308e2b71a97f9038204e208cf838bea6`  
		Last Modified: Tue, 26 Jul 2022 23:31:48 GMT  
		Size: 48.6 MB (48608834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4171261fac245494f48f61a9a3392736658b7c31f707783b796d952008ebb`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dcc6c8de93eee9106fbbff2915b00236e56b1bf820f724d87daae33cb57e8d`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39`

```console
$ docker pull mysql@sha256:b3a86578a582617214477d91e47e850f9e18df0b5d1644fb2d96d91a340b8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39` - linux; amd64

```console
$ docker pull mysql@sha256:5ecf646122c4fcbda81983c9e93e81a011b0593c9c19fbfc55b48bd1c23bc790
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147495b3a5ce957dee2319099a8808c1418e0b0a2c82c9b2396c5fb4b688509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:46:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:46:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:46:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:46:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 13 Jul 2022 06:46:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:46:49 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 26 Jul 2022 23:28:50 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Tue, 26 Jul 2022 23:28:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:29:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:29:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:29:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Tue, 26 Jul 2022 23:29:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:29:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:29:32 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:29:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:29:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:29:33 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:29:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ccd63cdb4ccb21c25d292be05bf37ee54a40a0746acdfa962a45a29a08b51`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f28a94c51f0d4090e9d6792e3ac48d318cc96056520dd0d7f6e6d2db851891`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 930.2 KB (930231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feea2a503b5e8b906b70f33abda7cc47dd30cb72363f804838831a48fdc8a74`  
		Last Modified: Wed, 13 Jul 2022 06:48:49 GMT  
		Size: 4.5 MB (4549473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd5852ecd934862db097d1380b3c2fe6471908610bbc2ac0b10f3daf59a183`  
		Last Modified: Wed, 13 Jul 2022 06:48:47 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5c3b24fd570d47fbe75cbe51b9f8428d58446368bf07022c42c52d943a9bb`  
		Last Modified: Tue, 26 Jul 2022 23:31:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a546386a618f1071083b0d9d357cceff83aa39db239224f71a97968e35fff2`  
		Last Modified: Tue, 26 Jul 2022 23:31:43 GMT  
		Size: 25.5 MB (25512706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b18297cf83f401e9641ba48cc9948ea3593821b42cae5990bacffd230c5ae5`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f23335fb87ecace32a157428c706c308e2b71a97f9038204e208cf838bea6`  
		Last Modified: Tue, 26 Jul 2022 23:31:48 GMT  
		Size: 48.6 MB (48608834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4171261fac245494f48f61a9a3392736658b7c31f707783b796d952008ebb`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dcc6c8de93eee9106fbbff2915b00236e56b1bf820f724d87daae33cb57e8d`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39-debian`

```console
$ docker pull mysql@sha256:8a2b6cea84dbac03339b72c39f0ac5be07816ad26e7f00ed2b1f13cba01512f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39-debian` - linux; amd64

```console
$ docker pull mysql@sha256:fea7de9666bd9c9afeb553ffc38f359372dcb5ceef2d93616dcd5d8d54aa2823
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162536048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93726b1fb68c052d2b8d15ec32edca75015c2b448a10acce6a4dacbce95a3fb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:24 GMT
ADD file:81dbfe4f9df4d280f7580380c0c5c93ba71fedba17b3072d2b7b4bce127f88a9 in / 
# Tue, 02 Aug 2022 01:20:24 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:52 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:58 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:50:06 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:50:07 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:50:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:50:14 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:50:14 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 02 Aug 2022 04:50:14 GMT
ENV MYSQL_VERSION=5.7.39-1debian10
# Tue, 02 Aug 2022 04:50:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:50:33 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:50:34 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:50:34 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:50:35 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:50:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:50:35 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:50:35 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:751ef25978b2971e15496369695ba51ed5b1b9aaca7e37b18a173d754d1ca820`  
		Last Modified: Tue, 02 Aug 2022 01:25:00 GMT  
		Size: 27.1 MB (27140083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dde536a29c092d40250b981fea24b05a9dc01fae8ed7473b95bc09a7919e3d4`  
		Last Modified: Tue, 02 Aug 2022 04:51:46 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6dbe684fb4d5f85516eab17e234538e624294dc9802813fe7d5471d7f0fb22`  
		Last Modified: Tue, 02 Aug 2022 04:51:45 GMT  
		Size: 4.2 MB (4179188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e7b9b4c2f95f52a2e335c627e253309b4990e6aa70126b87f466b03ead54a6`  
		Last Modified: Tue, 02 Aug 2022 04:51:44 GMT  
		Size: 1.4 MB (1386653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a63e201542d8ec3a607182805f0550389619da1b31e6b5565635bc9894dfb8`  
		Last Modified: Tue, 02 Aug 2022 04:51:44 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6f168d24831f4c6e191421ef112b0fd55a6bdf1e335246a8e3e6848d150c84`  
		Last Modified: Tue, 02 Aug 2022 04:51:47 GMT  
		Size: 14.1 MB (14087033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8f214492792e72d7b500c0a1e8e5df55d26bb07aa7c919911c04f1a9e7c1f2`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324d2966183c1fe326b26d0309659babda5141268f4e55ce8016cef16b6bcfc1`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294ee13b3a068f95d69addf91bb1ee6e73c9cb2b69798cdcf73ffa4be99e0cda`  
		Last Modified: Tue, 02 Aug 2022 04:51:57 GMT  
		Size: 115.7 MB (115733135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b412f4ed71e26e9a985d22750ab20a1a75d135bf32ece0b1c58093fb9407a814`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:664c9e63111cdb7e0c20a5b1cedfc5aec938f7eb9239d98209c8d34f2aa4000a`  
		Last Modified: Tue, 02 Aug 2022 04:51:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.39-oracle`

```console
$ docker pull mysql@sha256:b3a86578a582617214477d91e47e850f9e18df0b5d1644fb2d96d91a340b8972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.39-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:5ecf646122c4fcbda81983c9e93e81a011b0593c9c19fbfc55b48bd1c23bc790
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128373606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3147495b3a5ce957dee2319099a8808c1418e0b0a2c82c9b2396c5fb4b688509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:46:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:46:23 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:46:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:46:48 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 13 Jul 2022 06:46:49 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:46:49 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 26 Jul 2022 23:28:50 GMT
ENV MYSQL_VERSION=5.7.39-1.el7
# Tue, 26 Jul 2022 23:28:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:29:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:29:10 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:29:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el7
# Tue, 26 Jul 2022 23:29:31 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:29:32 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:29:32 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:29:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:29:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:29:33 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:29:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ccd63cdb4ccb21c25d292be05bf37ee54a40a0746acdfa962a45a29a08b51`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 870.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f28a94c51f0d4090e9d6792e3ac48d318cc96056520dd0d7f6e6d2db851891`  
		Last Modified: Wed, 13 Jul 2022 06:48:50 GMT  
		Size: 930.2 KB (930231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7feea2a503b5e8b906b70f33abda7cc47dd30cb72363f804838831a48fdc8a74`  
		Last Modified: Wed, 13 Jul 2022 06:48:49 GMT  
		Size: 4.5 MB (4549473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dd5852ecd934862db097d1380b3c2fe6471908610bbc2ac0b10f3daf59a183`  
		Last Modified: Wed, 13 Jul 2022 06:48:47 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5c3b24fd570d47fbe75cbe51b9f8428d58446368bf07022c42c52d943a9bb`  
		Last Modified: Tue, 26 Jul 2022 23:31:41 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a546386a618f1071083b0d9d357cceff83aa39db239224f71a97968e35fff2`  
		Last Modified: Tue, 26 Jul 2022 23:31:43 GMT  
		Size: 25.5 MB (25512706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b18297cf83f401e9641ba48cc9948ea3593821b42cae5990bacffd230c5ae5`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f23335fb87ecace32a157428c706c308e2b71a97f9038204e208cf838bea6`  
		Last Modified: Tue, 26 Jul 2022 23:31:48 GMT  
		Size: 48.6 MB (48608834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba4171261fac245494f48f61a9a3392736658b7c31f707783b796d952008ebb`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 5.2 KB (5162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96dcc6c8de93eee9106fbbff2915b00236e56b1bf820f724d87daae33cb57e8d`  
		Last Modified: Tue, 26 Jul 2022 23:31:39 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:25685dab065bbd127542768e3a697eefbaebb697d29b704d902af3f9930e55cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:36ba3720adcbd75f00da7680b25266ff480c6ce18265c9fc33daf8ff3886b48f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157835919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764b78482e3abe4d1ff03a987aee2f8293bd316233b0edaa2513ef582171a9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:07 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:49:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:49:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:23 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 02 Aug 2022 04:49:24 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:49:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:49:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:49:39 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 02 Aug 2022 04:49:39 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:49:40 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7d57630bf155b31f64dda3d9aad39f813d2fc58a320a985daebf3b14f3049`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012051d8478ee1090757968629c2716309d45c2643a5621613c61ab3a03d76c5`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 4.4 MB (4414798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ee4adc59fd6c63c76aee408f7e4da30281cd45d17e5a5719856fe1a23f1f`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 1.4 MB (1418429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be18bdc82a7cee346550f6df75908c04732f1cacc71c8c7f62f9e12f8cedeb`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704a769d13c18019727a01026cade3dbe37e10958126203da9485c5b5ef5395`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 12.7 MB (12661885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23293c50f7a9d512dc7ebeb4a7c6ad2d0986578db082bac560b47f82f20cff13`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321eeac21f74670a9c57774978f68de3eddd58873a14f2d6f670c4e34de9936`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08665c1f84bc1a553e1a74920208eb162f6a5f64d5cd874481a001360597920`  
		Last Modified: Tue, 02 Aug 2022 04:51:22 GMT  
		Size: 108.0 MB (107963250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04746e5f66aad7d8339336c409d924f925fa570241ec1c3b39c33bce9df68350`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25aec94921556ff0c94b5dc9bbc84c66e1c842d69e2948bc88ea5e4e76892e6`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 5.2 KB (5154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5f8572eba5ce08d6c92d90d8786c70833d8b03af10f67de7363d307e9e0a7`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:25685dab065bbd127542768e3a697eefbaebb697d29b704d902af3f9930e55cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:36ba3720adcbd75f00da7680b25266ff480c6ce18265c9fc33daf8ff3886b48f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157835919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764b78482e3abe4d1ff03a987aee2f8293bd316233b0edaa2513ef582171a9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:07 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:49:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:49:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:23 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 02 Aug 2022 04:49:24 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:49:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:49:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:49:39 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 02 Aug 2022 04:49:39 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:49:40 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7d57630bf155b31f64dda3d9aad39f813d2fc58a320a985daebf3b14f3049`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012051d8478ee1090757968629c2716309d45c2643a5621613c61ab3a03d76c5`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 4.4 MB (4414798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ee4adc59fd6c63c76aee408f7e4da30281cd45d17e5a5719856fe1a23f1f`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 1.4 MB (1418429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be18bdc82a7cee346550f6df75908c04732f1cacc71c8c7f62f9e12f8cedeb`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704a769d13c18019727a01026cade3dbe37e10958126203da9485c5b5ef5395`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 12.7 MB (12661885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23293c50f7a9d512dc7ebeb4a7c6ad2d0986578db082bac560b47f82f20cff13`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321eeac21f74670a9c57774978f68de3eddd58873a14f2d6f670c4e34de9936`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08665c1f84bc1a553e1a74920208eb162f6a5f64d5cd874481a001360597920`  
		Last Modified: Tue, 02 Aug 2022 04:51:22 GMT  
		Size: 108.0 MB (107963250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04746e5f66aad7d8339336c409d924f925fa570241ec1c3b39c33bce9df68350`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25aec94921556ff0c94b5dc9bbc84c66e1c842d69e2948bc88ea5e4e76892e6`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 5.2 KB (5154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5f8572eba5ce08d6c92d90d8786c70833d8b03af10f67de7363d307e9e0a7`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.30` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.30` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30-debian`

```console
$ docker pull mysql@sha256:25685dab065bbd127542768e3a697eefbaebb697d29b704d902af3f9930e55cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.30-debian` - linux; amd64

```console
$ docker pull mysql@sha256:36ba3720adcbd75f00da7680b25266ff480c6ce18265c9fc33daf8ff3886b48f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157835919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764b78482e3abe4d1ff03a987aee2f8293bd316233b0edaa2513ef582171a9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:07 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:49:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:49:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:23 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 02 Aug 2022 04:49:24 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:49:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:49:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:49:39 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 02 Aug 2022 04:49:39 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:49:40 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7d57630bf155b31f64dda3d9aad39f813d2fc58a320a985daebf3b14f3049`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012051d8478ee1090757968629c2716309d45c2643a5621613c61ab3a03d76c5`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 4.4 MB (4414798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ee4adc59fd6c63c76aee408f7e4da30281cd45d17e5a5719856fe1a23f1f`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 1.4 MB (1418429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be18bdc82a7cee346550f6df75908c04732f1cacc71c8c7f62f9e12f8cedeb`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704a769d13c18019727a01026cade3dbe37e10958126203da9485c5b5ef5395`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 12.7 MB (12661885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23293c50f7a9d512dc7ebeb4a7c6ad2d0986578db082bac560b47f82f20cff13`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321eeac21f74670a9c57774978f68de3eddd58873a14f2d6f670c4e34de9936`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08665c1f84bc1a553e1a74920208eb162f6a5f64d5cd874481a001360597920`  
		Last Modified: Tue, 02 Aug 2022 04:51:22 GMT  
		Size: 108.0 MB (107963250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04746e5f66aad7d8339336c409d924f925fa570241ec1c3b39c33bce9df68350`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25aec94921556ff0c94b5dc9bbc84c66e1c842d69e2948bc88ea5e4e76892e6`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 5.2 KB (5154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5f8572eba5ce08d6c92d90d8786c70833d8b03af10f67de7363d307e9e0a7`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.30-oracle`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.30-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.30-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:25685dab065bbd127542768e3a697eefbaebb697d29b704d902af3f9930e55cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:36ba3720adcbd75f00da7680b25266ff480c6ce18265c9fc33daf8ff3886b48f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157835919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764b78482e3abe4d1ff03a987aee2f8293bd316233b0edaa2513ef582171a9e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Aug 2022 01:20:04 GMT
ADD file:0eae0dca665c7044bf242cb1fc92cb8ea744f5af2dd376a558c90bc47349aefe in / 
# Tue, 02 Aug 2022 01:20:05 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 04:49:02 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 02 Aug 2022 04:49:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:07 GMT
ENV GOSU_VERSION=1.14
# Tue, 02 Aug 2022 04:49:16 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 02 Aug 2022 04:49:17 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 02 Aug 2022 04:49:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 04:49:23 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Aug 2022 04:49:24 GMT
ENV MYSQL_VERSION=8.0.30-1debian11
# Tue, 02 Aug 2022 04:49:24 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 02 Aug 2022 04:49:38 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 02 Aug 2022 04:49:39 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Aug 2022 04:49:39 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 02 Aug 2022 04:49:39 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 02 Aug 2022 04:49:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 02 Aug 2022 04:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Aug 2022 04:49:40 GMT
EXPOSE 3306 33060
# Tue, 02 Aug 2022 04:49:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:1efc276f4ff952c055dea726cfc96ec6a4fdb8b62d9eed816bd2b788f2860ad7`  
		Last Modified: Tue, 02 Aug 2022 01:24:13 GMT  
		Size: 31.4 MB (31366757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7d57630bf155b31f64dda3d9aad39f813d2fc58a320a985daebf3b14f3049`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:012051d8478ee1090757968629c2716309d45c2643a5621613c61ab3a03d76c5`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 4.4 MB (4414798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716ee4adc59fd6c63c76aee408f7e4da30281cd45d17e5a5719856fe1a23f1f`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 1.4 MB (1418429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56be18bdc82a7cee346550f6df75908c04732f1cacc71c8c7f62f9e12f8cedeb`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4704a769d13c18019727a01026cade3dbe37e10958126203da9485c5b5ef5395`  
		Last Modified: Tue, 02 Aug 2022 04:51:11 GMT  
		Size: 12.7 MB (12661885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23293c50f7a9d512dc7ebeb4a7c6ad2d0986578db082bac560b47f82f20cff13`  
		Last Modified: Tue, 02 Aug 2022 04:51:08 GMT  
		Size: 2.5 KB (2547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3321eeac21f74670a9c57774978f68de3eddd58873a14f2d6f670c4e34de9936`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b08665c1f84bc1a553e1a74920208eb162f6a5f64d5cd874481a001360597920`  
		Last Modified: Tue, 02 Aug 2022 04:51:22 GMT  
		Size: 108.0 MB (107963250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04746e5f66aad7d8339336c409d924f925fa570241ec1c3b39c33bce9df68350`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 844.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25aec94921556ff0c94b5dc9bbc84c66e1c842d69e2948bc88ea5e4e76892e6`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 5.2 KB (5154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f5f8572eba5ce08d6c92d90d8786c70833d8b03af10f67de7363d307e9e0a7`  
		Last Modified: Tue, 02 Aug 2022 04:51:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:4a215b02eeadcc01de50ce07176ee71cb9969d200da56f395dc5a576a77bb072
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:13b312e01e8c6eca35c0ff251c261ca2e52994b2a71890539ad31dce8978fa15
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132512841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38643ad93215bedea00fedd3d6f2a1c8e1bff3b9a172aa2547fd8b4bac9cfee3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Wed, 13 Jul 2022 06:44:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 13 Jul 2022 06:44:43 GMT
ENV GOSU_VERSION=1.14
# Wed, 13 Jul 2022 06:44:46 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 13 Jul 2022 06:45:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 13 Jul 2022 06:45:09 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 13 Jul 2022 06:45:09 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 26 Jul 2022 23:27:21 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:27:22 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 26 Jul 2022 23:27:50 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 26 Jul 2022 23:27:51 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 26 Jul 2022 23:27:51 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Tue, 26 Jul 2022 23:28:22 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 26 Jul 2022 23:28:23 GMT
VOLUME [/var/lib/mysql]
# Tue, 26 Jul 2022 23:28:23 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 26 Jul 2022 23:28:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 26 Jul 2022 23:28:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 26 Jul 2022 23:28:24 GMT
EXPOSE 3306 33060
# Tue, 26 Jul 2022 23:28:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327840d38cb25a590bbb16c433f0e05aa20ff9396d364afa42a6e26d24c6191c`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:642077275f5f571c8f25c08b96faa535499c0eda0abe5d31a1dd5652828833b6`  
		Last Modified: Wed, 13 Jul 2022 06:48:13 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e077469d560d641c3611653814fff9b3ae082c7b9fbdfb388a77ea34e49bf80f`  
		Last Modified: Wed, 13 Jul 2022 06:48:12 GMT  
		Size: 4.6 MB (4588162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf214d981a6cf5e7e8da61fc840f0f5500ea6b91512f990b91e2d1e8cd6bea1`  
		Last Modified: Wed, 13 Jul 2022 06:48:11 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4fda5f8b9a827b60600963d317db9cc284863fae5a963ba443cf2bb238f66c1`  
		Last Modified: Tue, 26 Jul 2022 23:30:30 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41c2763043bfe2e0ecad80d96d0a451f3ed7141c8241418f484cc787c12023c`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 47.7 MB (47732516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86b3df6abb1f7fd5fe173a37be422608072ee6ce831b964a3076473ac14105a`  
		Last Modified: Tue, 26 Jul 2022 23:30:29 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b1c2ed2ecfddca85150fe3e619638d7f71bcca106ad427e1fe8d513285a2fd`  
		Last Modified: Tue, 26 Jul 2022 23:30:36 GMT  
		Size: 40.0 MB (40031753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0edcd52771b148165e0ca520d3e3981ca95e94e9abcc3c895586a0caf919d7f`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 5.2 KB (5159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d312b5c835845f301e964bb6bd231671dc089225f6d4457eb636b7fabfad5e`  
		Last Modified: Tue, 26 Jul 2022 23:30:28 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:914ec0d396561e9ca92d8fdc1b5f618f3c261a3c202822c94e041ceeda4bed7a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.2 MB (141193486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56063370fd1666a88c9fc832d4401b10b47d7bd49c7013b3512c39787e5df89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 04 Aug 2022 00:40:43 GMT
ADD file:a68d82fa032efe6adc2926f7e745508f0541bba3f906e2702d34252353100747 in / 
# Thu, 04 Aug 2022 00:40:44 GMT
CMD ["/bin/bash"]
# Thu, 04 Aug 2022 00:57:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Thu, 04 Aug 2022 00:57:17 GMT
ENV GOSU_VERSION=1.14
# Thu, 04 Aug 2022 00:57:21 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 04 Aug 2022 00:57:44 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Thu, 04 Aug 2022 00:57:46 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Thu, 04 Aug 2022 00:57:47 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 04 Aug 2022 00:57:48 GMT
ENV MYSQL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:57:49 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Thu, 04 Aug 2022 00:58:17 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Thu, 04 Aug 2022 00:58:18 GMT
ENV MYSQL_SHELL_VERSION=8.0.30-1.el8
# Thu, 04 Aug 2022 00:58:50 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Thu, 04 Aug 2022 00:58:51 GMT
VOLUME [/var/lib/mysql]
# Thu, 04 Aug 2022 00:58:53 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Thu, 04 Aug 2022 00:58:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Thu, 04 Aug 2022 00:58:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 00:58:55 GMT
EXPOSE 3306 33060
# Thu, 04 Aug 2022 00:58:56 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ecf56004177eb6ca162c88de29e84bc4ba3d2e7efd3703df9ecae51b89003d52`  
		Last Modified: Thu, 04 Aug 2022 00:41:51 GMT  
		Size: 38.0 MB (38023046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091d9f012e1e44cf00d872494ff008feb11a824aa940f5fccaadcf0f043e951`  
		Last Modified: Thu, 04 Aug 2022 00:59:35 GMT  
		Size: 888.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabd9779d4678f8577c74505cc31bd42788a9ffa1eba563340b8ef29946b3e55`  
		Last Modified: Thu, 04 Aug 2022 00:59:36 GMT  
		Size: 857.2 KB (857152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6278448e2e194f0e2e8e7d2f29495296d594f7bd2e63d0306037e5b4f5125eb`  
		Last Modified: Thu, 04 Aug 2022 00:59:34 GMT  
		Size: 4.4 MB (4404159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6050832741b8d8e4dfba20e0d31c88f56b9b645c97752c9bbec708740c3e6e15`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0be9d1181fe5f7d6c39819a56c680e5e010a7b808b96eb00eabdeacd66ee6c1`  
		Last Modified: Thu, 04 Aug 2022 00:59:33 GMT  
		Size: 335.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdaffd3eb50f6880d4e27c2ba2a47193ba4e1959b4647e5e794b0872e981c5b`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 53.8 MB (53784614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74c1ad0f09fc99fb019bcbfebb1b57f4f7fcf7e968e6ece353a06d583cab8ed`  
		Last Modified: Thu, 04 Aug 2022 00:59:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad2b7db10f4eacccefc72231d395d9920b81dd4bba86be2a8994b8ee9161ec92`  
		Last Modified: Thu, 04 Aug 2022 00:59:38 GMT  
		Size: 44.1 MB (44115089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27624d90cadf384c8f6b5480da51cf29d2e860e488fb5a8f8336a5fd831fbfd`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 5.2 KB (5160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce107dc69a7b5a031fd79995ee9506e1a9c3148037b67fe726101e08e122895e`  
		Last Modified: Thu, 04 Aug 2022 00:59:30 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
