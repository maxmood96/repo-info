<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5-debian`](#mysql5-debian)
-	[`mysql:5-oracle`](#mysql5-oracle)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7-debian`](#mysql57-debian)
-	[`mysql:5.7-oracle`](#mysql57-oracle)
-	[`mysql:5.7.38`](#mysql5738)
-	[`mysql:5.7.38-debian`](#mysql5738-debian)
-	[`mysql:5.7.38-oracle`](#mysql5738-oracle)
-	[`mysql:8`](#mysql8)
-	[`mysql:8-debian`](#mysql8-debian)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0.29`](#mysql8029)
-	[`mysql:8.0.29-debian`](#mysql8029-debian)
-	[`mysql:8.0.29-oracle`](#mysql8029-oracle)
-	[`mysql:debian`](#mysqldebian)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)

## `mysql:5`

```console
$ docker pull mysql@sha256:4279d155f8cab19149c6078b20d53976f1498e31d6f848ac83e11323909b41f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:aadac0cb6207a1067dbac371f260cd51bf80a561e4cc35f106f514319444e974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e82e62381842f555f6e8b347645650c8b154746957044cd28c1f28b8817216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:39:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:39:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:39:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:39:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 05 Jul 2022 22:39:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 05 Jul 2022 22:39:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 05 Jul 2022 22:40:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:40:25 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:40:25 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:40:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7eaab7220f9e079d54a03c37fa84c5afc9d84f81e68fa61fa5fc06993d4057`  
		Last Modified: Tue, 05 Jul 2022 22:41:37 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e395314777250e8be8a06c1579128dac9ace727fd7a3a816d09fd4ba884d7`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f15c3a663d73b76dbb96e1453b906629a550ed892bf3d87078da35013f562`  
		Last Modified: Tue, 05 Jul 2022 22:41:35 GMT  
		Size: 4.5 MB (4549492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ee43a4e223812b066415c5b10428c8a4f89e639664d067cdbb3e0d21eba62`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28754770caaf5eaf0012288b220c9eb0babf5ca1005dbc36c06c7a0247270526`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebec8d1922fc2bc3a1c86438f4a2df654910365242554226a2ebd53443962e1`  
		Last Modified: Tue, 05 Jul 2022 22:41:36 GMT  
		Size: 25.5 MB (25495268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62114f2297745de3774bbe9750dd2c555fb12d0361cacddecb09c683e27ab6ac`  
		Last Modified: Tue, 05 Jul 2022 22:41:32 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8575f2324da2b151369ba4a069bf61a2d92902214feddd854aba5ee7a8ea6fb`  
		Last Modified: Tue, 05 Jul 2022 22:41:41 GMT  
		Size: 48.1 MB (48087864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c26cf546146d2767739d17bcad9059dcdc79342ad58ad80de3c712db7a9604`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 5.2 KB (5166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:4279d155f8cab19149c6078b20d53976f1498e31d6f848ac83e11323909b41f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:aadac0cb6207a1067dbac371f260cd51bf80a561e4cc35f106f514319444e974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e82e62381842f555f6e8b347645650c8b154746957044cd28c1f28b8817216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:39:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:39:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:39:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:39:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 05 Jul 2022 22:39:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 05 Jul 2022 22:39:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 05 Jul 2022 22:40:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:40:25 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:40:25 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:40:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7eaab7220f9e079d54a03c37fa84c5afc9d84f81e68fa61fa5fc06993d4057`  
		Last Modified: Tue, 05 Jul 2022 22:41:37 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e395314777250e8be8a06c1579128dac9ace727fd7a3a816d09fd4ba884d7`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f15c3a663d73b76dbb96e1453b906629a550ed892bf3d87078da35013f562`  
		Last Modified: Tue, 05 Jul 2022 22:41:35 GMT  
		Size: 4.5 MB (4549492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ee43a4e223812b066415c5b10428c8a4f89e639664d067cdbb3e0d21eba62`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28754770caaf5eaf0012288b220c9eb0babf5ca1005dbc36c06c7a0247270526`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebec8d1922fc2bc3a1c86438f4a2df654910365242554226a2ebd53443962e1`  
		Last Modified: Tue, 05 Jul 2022 22:41:36 GMT  
		Size: 25.5 MB (25495268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62114f2297745de3774bbe9750dd2c555fb12d0361cacddecb09c683e27ab6ac`  
		Last Modified: Tue, 05 Jul 2022 22:41:32 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8575f2324da2b151369ba4a069bf61a2d92902214feddd854aba5ee7a8ea6fb`  
		Last Modified: Tue, 05 Jul 2022 22:41:41 GMT  
		Size: 48.1 MB (48087864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c26cf546146d2767739d17bcad9059dcdc79342ad58ad80de3c712db7a9604`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 5.2 KB (5166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:4279d155f8cab19149c6078b20d53976f1498e31d6f848ac83e11323909b41f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:aadac0cb6207a1067dbac371f260cd51bf80a561e4cc35f106f514319444e974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e82e62381842f555f6e8b347645650c8b154746957044cd28c1f28b8817216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:39:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:39:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:39:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:39:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 05 Jul 2022 22:39:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 05 Jul 2022 22:39:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 05 Jul 2022 22:40:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:40:25 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:40:25 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:40:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7eaab7220f9e079d54a03c37fa84c5afc9d84f81e68fa61fa5fc06993d4057`  
		Last Modified: Tue, 05 Jul 2022 22:41:37 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e395314777250e8be8a06c1579128dac9ace727fd7a3a816d09fd4ba884d7`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f15c3a663d73b76dbb96e1453b906629a550ed892bf3d87078da35013f562`  
		Last Modified: Tue, 05 Jul 2022 22:41:35 GMT  
		Size: 4.5 MB (4549492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ee43a4e223812b066415c5b10428c8a4f89e639664d067cdbb3e0d21eba62`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28754770caaf5eaf0012288b220c9eb0babf5ca1005dbc36c06c7a0247270526`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebec8d1922fc2bc3a1c86438f4a2df654910365242554226a2ebd53443962e1`  
		Last Modified: Tue, 05 Jul 2022 22:41:36 GMT  
		Size: 25.5 MB (25495268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62114f2297745de3774bbe9750dd2c555fb12d0361cacddecb09c683e27ab6ac`  
		Last Modified: Tue, 05 Jul 2022 22:41:32 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8575f2324da2b151369ba4a069bf61a2d92902214feddd854aba5ee7a8ea6fb`  
		Last Modified: Tue, 05 Jul 2022 22:41:41 GMT  
		Size: 48.1 MB (48087864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c26cf546146d2767739d17bcad9059dcdc79342ad58ad80de3c712db7a9604`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 5.2 KB (5166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:4279d155f8cab19149c6078b20d53976f1498e31d6f848ac83e11323909b41f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:aadac0cb6207a1067dbac371f260cd51bf80a561e4cc35f106f514319444e974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e82e62381842f555f6e8b347645650c8b154746957044cd28c1f28b8817216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:39:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:39:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:39:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:39:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 05 Jul 2022 22:39:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 05 Jul 2022 22:39:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 05 Jul 2022 22:40:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:40:25 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:40:25 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:40:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7eaab7220f9e079d54a03c37fa84c5afc9d84f81e68fa61fa5fc06993d4057`  
		Last Modified: Tue, 05 Jul 2022 22:41:37 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e395314777250e8be8a06c1579128dac9ace727fd7a3a816d09fd4ba884d7`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f15c3a663d73b76dbb96e1453b906629a550ed892bf3d87078da35013f562`  
		Last Modified: Tue, 05 Jul 2022 22:41:35 GMT  
		Size: 4.5 MB (4549492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ee43a4e223812b066415c5b10428c8a4f89e639664d067cdbb3e0d21eba62`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28754770caaf5eaf0012288b220c9eb0babf5ca1005dbc36c06c7a0247270526`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebec8d1922fc2bc3a1c86438f4a2df654910365242554226a2ebd53443962e1`  
		Last Modified: Tue, 05 Jul 2022 22:41:36 GMT  
		Size: 25.5 MB (25495268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62114f2297745de3774bbe9750dd2c555fb12d0361cacddecb09c683e27ab6ac`  
		Last Modified: Tue, 05 Jul 2022 22:41:32 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8575f2324da2b151369ba4a069bf61a2d92902214feddd854aba5ee7a8ea6fb`  
		Last Modified: Tue, 05 Jul 2022 22:41:41 GMT  
		Size: 48.1 MB (48087864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c26cf546146d2767739d17bcad9059dcdc79342ad58ad80de3c712db7a9604`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 5.2 KB (5166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38`

```console
$ docker pull mysql@sha256:4279d155f8cab19149c6078b20d53976f1498e31d6f848ac83e11323909b41f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38` - linux; amd64

```console
$ docker pull mysql@sha256:aadac0cb6207a1067dbac371f260cd51bf80a561e4cc35f106f514319444e974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e82e62381842f555f6e8b347645650c8b154746957044cd28c1f28b8817216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:39:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:39:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:39:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:39:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 05 Jul 2022 22:39:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 05 Jul 2022 22:39:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 05 Jul 2022 22:40:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:40:25 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:40:25 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:40:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7eaab7220f9e079d54a03c37fa84c5afc9d84f81e68fa61fa5fc06993d4057`  
		Last Modified: Tue, 05 Jul 2022 22:41:37 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e395314777250e8be8a06c1579128dac9ace727fd7a3a816d09fd4ba884d7`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f15c3a663d73b76dbb96e1453b906629a550ed892bf3d87078da35013f562`  
		Last Modified: Tue, 05 Jul 2022 22:41:35 GMT  
		Size: 4.5 MB (4549492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ee43a4e223812b066415c5b10428c8a4f89e639664d067cdbb3e0d21eba62`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28754770caaf5eaf0012288b220c9eb0babf5ca1005dbc36c06c7a0247270526`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebec8d1922fc2bc3a1c86438f4a2df654910365242554226a2ebd53443962e1`  
		Last Modified: Tue, 05 Jul 2022 22:41:36 GMT  
		Size: 25.5 MB (25495268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62114f2297745de3774bbe9750dd2c555fb12d0361cacddecb09c683e27ab6ac`  
		Last Modified: Tue, 05 Jul 2022 22:41:32 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8575f2324da2b151369ba4a069bf61a2d92902214feddd854aba5ee7a8ea6fb`  
		Last Modified: Tue, 05 Jul 2022 22:41:41 GMT  
		Size: 48.1 MB (48087864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c26cf546146d2767739d17bcad9059dcdc79342ad58ad80de3c712db7a9604`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 5.2 KB (5166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-debian`

```console
$ docker pull mysql@sha256:8b4b41d530c40d77a3205c53f7ecf1026d735648d9a09777845f305953e5eff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:e73f0d1cb2e042d4b93fcd4a301c147cbc0a28e982c0e965901162a733991df6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162479495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa50097efbdef5884e5ebaba4da5899e79609b78cd4fe91b365d5d9d3205188`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:46 GMT
ADD file:0ae121f9805d31a4ad0ed63e1fc397167a23656a285572fe68bfc51ea91ecfdd in / 
# Thu, 23 Jun 2022 00:20:46 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 04:05:30 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Thu, 23 Jun 2022 04:05:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 04:05:35 GMT
ENV GOSU_VERSION=1.14
# Thu, 23 Jun 2022 04:05:44 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 23 Jun 2022 04:05:45 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 28 Jun 2022 00:21:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 Jun 2022 00:21:38 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 28 Jun 2022 00:23:07 GMT
ENV MYSQL_VERSION=5.7.38-1debian10
# Tue, 28 Jun 2022 00:23:08 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 28 Jun 2022 00:23:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 28 Jun 2022 00:23:26 GMT
VOLUME [/var/lib/mysql]
# Tue, 28 Jun 2022 00:23:26 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 28 Jun 2022 00:23:27 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 28 Jun 2022 00:23:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 Jun 2022 00:23:27 GMT
EXPOSE 3306 33060
# Tue, 28 Jun 2022 00:23:27 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:824b15f81d6568adc139263c39805e52d9880758b907f40144bbb1938ca59323`  
		Last Modified: Thu, 23 Jun 2022 00:26:03 GMT  
		Size: 27.1 MB (27140043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c559dd1913db86c3984c4dfc3e07fccee1fecc810999b4b6aea8b5cde104d207`  
		Last Modified: Thu, 23 Jun 2022 04:07:11 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e201c19614e69f7e7040b951f02b91baf11428b0f83cab3516df27a8f4a79870`  
		Last Modified: Thu, 23 Jun 2022 04:07:12 GMT  
		Size: 4.2 MB (4179291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4247e8f61251b7262eb83877350fc1c641526969e1ce931ec6d78361cb9236c`  
		Last Modified: Thu, 23 Jun 2022 04:07:10 GMT  
		Size: 1.4 MB (1386689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc9fefd8cfb55346940b7d843ac4d88addc2a66b38e85f7b1c0b94820ce698ca`  
		Last Modified: Thu, 23 Jun 2022 04:07:09 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3787edd16df30d4ca1f062e3becefcf1e1f5595517d4325c48006156f358ee`  
		Last Modified: Tue, 28 Jun 2022 00:24:23 GMT  
		Size: 14.1 MB (14086998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6bb40f875d341e08634fbde0893016a25f4a8a6777248ef3ff6ecdd8b0f0a3d`  
		Last Modified: Tue, 28 Jun 2022 00:24:20 GMT  
		Size: 2.5 KB (2548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09914736f6f7304f95bac6a69ac7c684924e69e590068525ba1e3bcf61c6202c`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 254.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32c835958ed8cedc7d60d07e83078b5dfa1b9b573b8e18cdc693feec0d92b591`  
		Last Modified: Tue, 28 Jun 2022 00:25:40 GMT  
		Size: 115.7 MB (115676518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa6834c9208751015a2687822d5a5142bfd1b52ce353eb0030ed8c45bc25662`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 5.2 KB (5157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf3b0798493943a172317b25ea1bc22652422af88c2954947e1e3342edcac2d`  
		Last Modified: Tue, 28 Jun 2022 00:25:25 GMT  
		Size: 118.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.38-oracle`

```console
$ docker pull mysql@sha256:4279d155f8cab19149c6078b20d53976f1498e31d6f848ac83e11323909b41f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:aadac0cb6207a1067dbac371f260cd51bf80a561e4cc35f106f514319444e974
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.8 MB (127835289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e82e62381842f555f6e8b347645650c8b154746957044cd28c1f28b8817216`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:58 GMT
ADD file:50fb7d83a9d57e5a0a6af5e5daf27e464ae8a28c196ce6bad6c254dfc1774cdd in / 
# Tue, 05 Jul 2022 22:20:58 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:39:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:39:25 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:39:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:39:44 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Tue, 05 Jul 2022 22:39:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 05 Jul 2022 22:39:45 GMT
ENV MYSQL_VERSION=5.7.38-1.el7
# Tue, 05 Jul 2022 22:39:46 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:40:03 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:40:03 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el7
# Tue, 05 Jul 2022 22:40:24 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:40:25 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:40:25 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:40:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:40:25 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:40:25 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:66fb3478003364657ac7751c40e41a135e02975f9459f652b1df23e3896b5fac`  
		Last Modified: Tue, 05 Jul 2022 22:22:18 GMT  
		Size: 48.8 MB (48762895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b7eaab7220f9e079d54a03c37fa84c5afc9d84f81e68fa61fa5fc06993d4057`  
		Last Modified: Tue, 05 Jul 2022 22:41:37 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8e395314777250e8be8a06c1579128dac9ace727fd7a3a816d09fd4ba884d7`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 930.2 KB (930228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03f15c3a663d73b76dbb96e1453b906629a550ed892bf3d87078da35013f562`  
		Last Modified: Tue, 05 Jul 2022 22:41:35 GMT  
		Size: 4.5 MB (4549492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398ee43a4e223812b066415c5b10428c8a4f89e639664d067cdbb3e0d21eba62`  
		Last Modified: Tue, 05 Jul 2022 22:41:34 GMT  
		Size: 2.7 KB (2659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28754770caaf5eaf0012288b220c9eb0babf5ca1005dbc36c06c7a0247270526`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebec8d1922fc2bc3a1c86438f4a2df654910365242554226a2ebd53443962e1`  
		Last Modified: Tue, 05 Jul 2022 22:41:36 GMT  
		Size: 25.5 MB (25495268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62114f2297745de3774bbe9750dd2c555fb12d0361cacddecb09c683e27ab6ac`  
		Last Modified: Tue, 05 Jul 2022 22:41:32 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8575f2324da2b151369ba4a069bf61a2d92902214feddd854aba5ee7a8ea6fb`  
		Last Modified: Tue, 05 Jul 2022 22:41:41 GMT  
		Size: 48.1 MB (48087864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c26cf546146d2767739d17bcad9059dcdc79342ad58ad80de3c712db7a9604`  
		Last Modified: Tue, 05 Jul 2022 22:41:31 GMT  
		Size: 5.2 KB (5166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:59ffc15bb9ff6c45728942f5782d63802c0b365ff0570a6461755b043c24c5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:a64df27bf8864ca04823b2a3bed3e663a323317617e6ad3cbf44656b0fe49e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157623333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0429521d998bf30471f57c7996e62ff4a5fa1a02c2a38f9719b3b3530e5886e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Tue, 05 Jul 2022 18:49:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Jul 2022 18:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:12 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 18:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 18:49:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 18:49:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 18:49:28 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 18:49:29 GMT
ENV MYSQL_VERSION=8.0.29-1debian11
# Tue, 05 Jul 2022 18:49:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 05 Jul 2022 18:49:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 05 Jul 2022 18:49:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 18:49:44 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 05 Jul 2022 18:49:44 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 18:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Jul 2022 18:49:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 18:49:45 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 18:49:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb421c0470dcc46febaa73c93d783d0e73d6ffc27390165ad0c6c05240d229`  
		Last Modified: Tue, 05 Jul 2022 18:50:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8913f7af8789b7c5e495708ebcb5bc717e72e314ff1c75e2f33f8b2291b28c4`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 4.6 MB (4644195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b5a0749b5b0e1ca4d21aa28341fe395d1b1f4bcef393a08ddffda67387ce26`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 1.4 MB (1418566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c1e6766449721ee016dc3a8915e1c0223455ca68a7d8cbc98bc3ee1c8ce6b`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d053cd43ebdcbc601b661e1310dfa0f0a3ffa3270727a54211d556578bdb7e1f`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 12.7 MB (12662096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c8f03894adcd4e3de9c8daa388adcd2d8b0f20bf560c9808b7313879153561`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6680724c36114e984b67e921ae9e4438aae29a220be32f3c09aab36e688259`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1360acd4b871d5886f29dfa0f7c17ed71269ce40ca12ebb1f629f109586a56`  
		Last Modified: Tue, 05 Jul 2022 18:50:50 GMT  
		Size: 107.5 MB (107508256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94f90c6b4a5d2709d28586f57c8e0f7348441a795adec5a0f8b7e3469968483`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b1f20b352596d8b7ee0bdc29fd584261942d04d6c9190ec1975316b567c44`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398113cf1a18167e2bd9462511531bd2c98fdafefdb3317fef5ebc18e01fdafa`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:59ffc15bb9ff6c45728942f5782d63802c0b365ff0570a6461755b043c24c5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:a64df27bf8864ca04823b2a3bed3e663a323317617e6ad3cbf44656b0fe49e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157623333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0429521d998bf30471f57c7996e62ff4a5fa1a02c2a38f9719b3b3530e5886e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Tue, 05 Jul 2022 18:49:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Jul 2022 18:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:12 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 18:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 18:49:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 18:49:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 18:49:28 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 18:49:29 GMT
ENV MYSQL_VERSION=8.0.29-1debian11
# Tue, 05 Jul 2022 18:49:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 05 Jul 2022 18:49:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 05 Jul 2022 18:49:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 18:49:44 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 05 Jul 2022 18:49:44 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 18:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Jul 2022 18:49:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 18:49:45 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 18:49:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb421c0470dcc46febaa73c93d783d0e73d6ffc27390165ad0c6c05240d229`  
		Last Modified: Tue, 05 Jul 2022 18:50:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8913f7af8789b7c5e495708ebcb5bc717e72e314ff1c75e2f33f8b2291b28c4`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 4.6 MB (4644195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b5a0749b5b0e1ca4d21aa28341fe395d1b1f4bcef393a08ddffda67387ce26`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 1.4 MB (1418566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c1e6766449721ee016dc3a8915e1c0223455ca68a7d8cbc98bc3ee1c8ce6b`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d053cd43ebdcbc601b661e1310dfa0f0a3ffa3270727a54211d556578bdb7e1f`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 12.7 MB (12662096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c8f03894adcd4e3de9c8daa388adcd2d8b0f20bf560c9808b7313879153561`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6680724c36114e984b67e921ae9e4438aae29a220be32f3c09aab36e688259`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1360acd4b871d5886f29dfa0f7c17ed71269ce40ca12ebb1f629f109586a56`  
		Last Modified: Tue, 05 Jul 2022 18:50:50 GMT  
		Size: 107.5 MB (107508256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94f90c6b4a5d2709d28586f57c8e0f7348441a795adec5a0f8b7e3469968483`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b1f20b352596d8b7ee0bdc29fd584261942d04d6c9190ec1975316b567c44`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398113cf1a18167e2bd9462511531bd2c98fdafefdb3317fef5ebc18e01fdafa`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.29` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.29` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-debian`

```console
$ docker pull mysql@sha256:59ffc15bb9ff6c45728942f5782d63802c0b365ff0570a6461755b043c24c5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.29-debian` - linux; amd64

```console
$ docker pull mysql@sha256:a64df27bf8864ca04823b2a3bed3e663a323317617e6ad3cbf44656b0fe49e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157623333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0429521d998bf30471f57c7996e62ff4a5fa1a02c2a38f9719b3b3530e5886e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Tue, 05 Jul 2022 18:49:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Jul 2022 18:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:12 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 18:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 18:49:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 18:49:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 18:49:28 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 18:49:29 GMT
ENV MYSQL_VERSION=8.0.29-1debian11
# Tue, 05 Jul 2022 18:49:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 05 Jul 2022 18:49:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 05 Jul 2022 18:49:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 18:49:44 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 05 Jul 2022 18:49:44 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 18:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Jul 2022 18:49:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 18:49:45 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 18:49:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb421c0470dcc46febaa73c93d783d0e73d6ffc27390165ad0c6c05240d229`  
		Last Modified: Tue, 05 Jul 2022 18:50:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8913f7af8789b7c5e495708ebcb5bc717e72e314ff1c75e2f33f8b2291b28c4`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 4.6 MB (4644195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b5a0749b5b0e1ca4d21aa28341fe395d1b1f4bcef393a08ddffda67387ce26`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 1.4 MB (1418566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c1e6766449721ee016dc3a8915e1c0223455ca68a7d8cbc98bc3ee1c8ce6b`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d053cd43ebdcbc601b661e1310dfa0f0a3ffa3270727a54211d556578bdb7e1f`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 12.7 MB (12662096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c8f03894adcd4e3de9c8daa388adcd2d8b0f20bf560c9808b7313879153561`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6680724c36114e984b67e921ae9e4438aae29a220be32f3c09aab36e688259`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1360acd4b871d5886f29dfa0f7c17ed71269ce40ca12ebb1f629f109586a56`  
		Last Modified: Tue, 05 Jul 2022 18:50:50 GMT  
		Size: 107.5 MB (107508256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94f90c6b4a5d2709d28586f57c8e0f7348441a795adec5a0f8b7e3469968483`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b1f20b352596d8b7ee0bdc29fd584261942d04d6c9190ec1975316b567c44`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398113cf1a18167e2bd9462511531bd2c98fdafefdb3317fef5ebc18e01fdafa`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.29-oracle`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.29-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.29-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:59ffc15bb9ff6c45728942f5782d63802c0b365ff0570a6461755b043c24c5ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:a64df27bf8864ca04823b2a3bed3e663a323317617e6ad3cbf44656b0fe49e8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157623333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0429521d998bf30471f57c7996e62ff4a5fa1a02c2a38f9719b3b3530e5886e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Tue, 05 Jul 2022 18:49:06 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 05 Jul 2022 18:49:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:12 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 18:49:21 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 18:49:22 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 18:49:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 05 Jul 2022 18:49:28 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 18:49:28 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 18:49:29 GMT
ENV MYSQL_VERSION=8.0.29-1debian11
# Tue, 05 Jul 2022 18:49:29 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 05 Jul 2022 18:49:43 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 05 Jul 2022 18:49:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 18:49:44 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 05 Jul 2022 18:49:44 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 18:49:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 05 Jul 2022 18:49:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 18:49:45 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 18:49:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0acb421c0470dcc46febaa73c93d783d0e73d6ffc27390165ad0c6c05240d229`  
		Last Modified: Tue, 05 Jul 2022 18:50:38 GMT  
		Size: 1.7 KB (1739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8913f7af8789b7c5e495708ebcb5bc717e72e314ff1c75e2f33f8b2291b28c4`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 4.6 MB (4644195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b5a0749b5b0e1ca4d21aa28341fe395d1b1f4bcef393a08ddffda67387ce26`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 1.4 MB (1418566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41c1e6766449721ee016dc3a8915e1c0223455ca68a7d8cbc98bc3ee1c8ce6b`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d053cd43ebdcbc601b661e1310dfa0f0a3ffa3270727a54211d556578bdb7e1f`  
		Last Modified: Tue, 05 Jul 2022 18:50:39 GMT  
		Size: 12.7 MB (12662096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c8f03894adcd4e3de9c8daa388adcd2d8b0f20bf560c9808b7313879153561`  
		Last Modified: Tue, 05 Jul 2022 18:50:36 GMT  
		Size: 2.5 KB (2550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6680724c36114e984b67e921ae9e4438aae29a220be32f3c09aab36e688259`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1360acd4b871d5886f29dfa0f7c17ed71269ce40ca12ebb1f629f109586a56`  
		Last Modified: Tue, 05 Jul 2022 18:50:50 GMT  
		Size: 107.5 MB (107508256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94f90c6b4a5d2709d28586f57c8e0f7348441a795adec5a0f8b7e3469968483`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 845.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b1f20b352596d8b7ee0bdc29fd584261942d04d6c9190ec1975316b567c44`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 5.2 KB (5158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:398113cf1a18167e2bd9462511531bd2c98fdafefdb3317fef5ebc18e01fdafa`  
		Last Modified: Tue, 05 Jul 2022 18:50:34 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:444f037733d01fc3dfc691a9ab05e346629e8e4d3a6c75da864f21421fb38ced
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:079ee165f9d2b36e855d4e096dc48c57990cf2ccd2232a9399deffb9e220db9a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.8 MB (131790777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e458be53cabe4d12b9d6d18511445d79ee96ef00441a23a6d1eab279d99a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:20:34 GMT
ADD file:69555d6633d88e50ab2ddecc8bc5002a8f79005d828a9093975d68ca05b023e9 in / 
# Tue, 05 Jul 2022 22:20:34 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 22:37:44 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 22:37:44 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 22:37:48 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 22:38:09 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 22:38:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 22:38:10 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:38:11 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 22:38:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 22:38:38 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 22:38:38 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 22:39:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 22:39:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 22:39:09 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 22:39:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 22:39:09 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 22:39:09 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e54b73e95ef388354463a761e4e93ce3dac29cb244b2dc0424f2f4afc6ddf5cd`  
		Last Modified: Tue, 05 Jul 2022 22:21:41 GMT  
		Size: 39.2 MB (39222121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb429e544310419a3cd729479c47eb7b834676be1ac091dff00e8087402d8c97`  
		Last Modified: Tue, 05 Jul 2022 22:41:01 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c148b3f9047c21af681257a3301bc925e1a63a6071ca04137df7e8e5ac15e778`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 928.8 KB (928836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1dd213a3236752eb500bedc1296fcd8b9485906292cb9a358cba5c0c38ded31`  
		Last Modified: Tue, 05 Jul 2022 22:40:59 GMT  
		Size: 4.6 MB (4588185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297095d1476d409ad25b3ba8fe91e2d57ef51d3b241935180ac85517c1502ae1`  
		Last Modified: Tue, 05 Jul 2022 22:40:58 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f3aa8373015766399afc3280b7482559b01b7e66cf7a908895b763411030ac`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350194364819a9e2eed735d032609aaf9fe69b6d270e0a6cc41469a57af840e`  
		Last Modified: Tue, 05 Jul 2022 22:41:03 GMT  
		Size: 47.3 MB (47260578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23722cff1cc365fa44e2d131fab041780a96ae21fac7d377f5bd228c8b3261f9`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb19883dc4c6df1517140f07ec2cdebddb0a1337388ffd6f0926616c86021f3e`  
		Last Modified: Tue, 05 Jul 2022 22:41:04 GMT  
		Size: 39.8 MB (39781531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eaa2c23609563b5d81f97470ce85037d66b4fcc9fbdb10dab332c0d8b1bce40`  
		Last Modified: Tue, 05 Jul 2022 22:40:56 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ceb04a9eddc1d2ef38b55bef0b9fc7072902473b73fb136afecde3b3a0148897
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e1d555ec0307e2e7c4d51ffcff202945ba33ec85df988f5136b868b409d220`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 05 Jul 2022 22:43:14 GMT
ADD file:e864e9187ff57bc1df9611a0990052f89611bfe7b6bc8e3d24b500b0886ec725 in / 
# Tue, 05 Jul 2022 22:43:14 GMT
CMD ["/bin/bash"]
# Tue, 05 Jul 2022 23:00:28 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql; 		mkdir /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d
# Tue, 05 Jul 2022 23:00:29 GMT
ENV GOSU_VERSION=1.14
# Tue, 05 Jul 2022 23:00:33 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 05 Jul 2022 23:00:58 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Tue, 05 Jul 2022 23:00:59 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Tue, 05 Jul 2022 23:01:00 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 05 Jul 2022 23:01:01 GMT
ENV MYSQL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:02 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 05 Jul 2022 23:01:27 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 		mysqld --version; 	mysql --version
# Tue, 05 Jul 2022 23:01:28 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 05 Jul 2022 23:01:29 GMT
ENV MYSQL_SHELL_VERSION=8.0.29-1.el8
# Tue, 05 Jul 2022 23:01:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 05 Jul 2022 23:02:00 GMT
VOLUME [/var/lib/mysql]
# Tue, 05 Jul 2022 23:02:01 GMT
COPY file:d27cf504fa76fb5a4038020a01eaaf52723b17b751566119de311adacb043752 in /usr/local/bin/ 
# Tue, 05 Jul 2022 23:02:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 05 Jul 2022 23:02:02 GMT
EXPOSE 3306 33060
# Tue, 05 Jul 2022 23:02:03 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e5d41499b4049578ed8bbb14817cd79d4136a84899b65e4364b0125d4d1c792c`  
		Last Modified: Tue, 05 Jul 2022 22:44:31 GMT  
		Size: 38.0 MB (38027757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac26e2263029d9a168f2f2d81f9ec1b096ad80d339f586fb913592d6166285aa`  
		Last Modified: Tue, 05 Jul 2022 23:02:32 GMT  
		Size: 1.0 KB (1015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3afc17806d6cf9933e14c2a9a8a1d62527026d4198cd5b89a858594cf9204af`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 857.2 KB (857153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43b85b9ce04e8230eebf27fd5e2216de019c958974e9ad3f5ea88eeb630944e`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 4.4 MB (4421797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f258fccfce452f5f019194ed22d62872644aa1477dd262a1b143ef0756030f6`  
		Last Modified: Tue, 05 Jul 2022 23:02:30 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c3a1177329308f038bf0b8e09cd3b212ff1a8b60f57ad55df01c6f923950009`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370b8648f9c7ef3ed498bbc50a4d273ae906a5444a4c58aeda6e5b195d96d9a8`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 53.3 MB (53324695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292fcdc1cd4bb0768c72bbae039b2645e9c5b1b11d19d3c7d22152f87d1e0600`  
		Last Modified: Tue, 05 Jul 2022 23:02:27 GMT  
		Size: 316.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e8e0d9d2d20f66619d736ceac11d25b7564141e3c447229b85270553953f6e`  
		Last Modified: Tue, 05 Jul 2022 23:02:35 GMT  
		Size: 42.1 MB (42075205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526b98447ca065bab0d1dc82a01b080d3bedd2610f34a194ef6cca9d5c77f8b0`  
		Last Modified: Tue, 05 Jul 2022 23:02:28 GMT  
		Size: 5.2 KB (5163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
