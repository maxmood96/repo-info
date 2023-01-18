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
$ docker pull mysql@sha256:f04fc2e2f01e65d6e2828b4cce2c4761d9258aee71d989e273b2ae309f44a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:8dae5a91219c1789ba43690412f6319ae96f51d8787ce81f820907bff6e6c786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129279340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982339a20a53052bd5f2b2e8438b3c95c91013f653ee781a67934cd1f9f9631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:23:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:23:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:23:52 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:24:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 07 Dec 2022 02:24:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:24:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:07:55 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Tue, 17 Jan 2023 21:07:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:08:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:08:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:08:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Tue, 17 Jan 2023 21:08:41 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:08:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:08:42 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:08:43 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:08:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9d8a3567e30df99576e0a4dbca773af581230fee203891610e6ccbdaa823d2`  
		Last Modified: Wed, 07 Dec 2022 02:26:00 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1f0f349e08af59ed77c7d56ede70f0c5739daa2477ef54a4ee457f5e3e47`  
		Last Modified: Wed, 07 Dec 2022 02:26:01 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff8dfb9b12b027c35d779fe4f06a9b3d0d26efed52153324cfa2f409423b0d`  
		Last Modified: Wed, 07 Dec 2022 02:25:59 GMT  
		Size: 4.5 MB (4539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56cbebc916d35659623816867a456610961f77db6d9753e738c5564651dfa0`  
		Last Modified: Wed, 07 Dec 2022 02:25:58 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7bdfff0f5b940a8450ad5ef0f25d73f40cc8cc13627bda09a9586e81b74502`  
		Last Modified: Tue, 17 Jan 2023 21:10:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7677d20b791d5ee29bf70cce20582fa06c3634201945e98b8501f20a5f9f0da`  
		Last Modified: Tue, 17 Jan 2023 21:10:58 GMT  
		Size: 25.5 MB (25532144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bcfc1167c2472c268123c91440454fe1d68088dce3be90dae9b1fdf1080640`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c0b71b700b5f8b16e6ac83e1bb437b60e10229f74fbc58518cc4c621cf61`  
		Last Modified: Tue, 17 Jan 2023 21:11:03 GMT  
		Size: 48.4 MB (48449762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa2e026ac3ff90ad7fe835692787abbda5ed6bd469edfa416b1c42f331f78f`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b784fa66c50879ee479e3153e735b274ebd3be28d34000d375ef2462f668446`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-debian`

```console
$ docker pull mysql@sha256:6f4fb1b8c2717cbe709e755f83a3d6f52dabe58902569bdaa14d0cc9d4c18d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-debian` - linux; amd64

```console
$ docker pull mysql@sha256:603b9b890043bd774c673060292c818e771135c51d0d2b8b7873151906610220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162644100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4726a7600c6f5c8b58d26e8a5634a13bdff727ee29eebe5edbf9ebdd00533898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:20:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:20:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:20:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:20:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:20:36 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:08:53 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Tue, 17 Jan 2023 21:08:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:09:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:09:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:09:17 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:09:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:09:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:09:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702e45a0d0fab46740d0cf404969001dc0537dd564973fa6f31da2a00cfe5ef8`  
		Last Modified: Wed, 11 Jan 2023 06:22:03 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad96d17a23a7cff619709675f8981274e6a4ff7a9fb99590f0a837511e69a50b`  
		Last Modified: Wed, 11 Jan 2023 06:22:03 GMT  
		Size: 4.2 MB (4182274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1832d5509d3dce5314c5ffb58ac35ef7e35c396457e6fab747267312751708cf`  
		Last Modified: Wed, 11 Jan 2023 06:22:02 GMT  
		Size: 1.4 MB (1388883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a580bc4aa47839f3f325b0a7bd7f927d8f41bb947a8e6d1847048a16c88dc`  
		Last Modified: Wed, 11 Jan 2023 06:22:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562f0a131c6cc56e3a6b85245641c4251cb4bc5e5b97f08d5d97209b8c11c38c`  
		Last Modified: Wed, 11 Jan 2023 06:22:04 GMT  
		Size: 14.1 MB (14089400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5760997e25e0fd516f2aab1a32be22ae0a919faa2c2dd36a3ad098d772ca3495`  
		Last Modified: Wed, 11 Jan 2023 06:22:00 GMT  
		Size: 2.5 KB (2543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2459447ebb40538b162dbc50dd435551e3c63d290fc1fb37555ee724a56989a9`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b7ab69b071a7139fbe466170a22caead38334834a792630c6a0e9b12f15ef6`  
		Last Modified: Tue, 17 Jan 2023 21:11:37 GMT  
		Size: 115.8 MB (115832999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aad2d01a4e6a079bc797ac021db4938622225182fa24eab797ee661d30134e9`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d70cf470197d6c4c9c3f0789a15440b5439ac8536ea8db923608b24b7dfc59`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5-oracle`

```console
$ docker pull mysql@sha256:f04fc2e2f01e65d6e2828b4cce2c4761d9258aee71d989e273b2ae309f44a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8dae5a91219c1789ba43690412f6319ae96f51d8787ce81f820907bff6e6c786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129279340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982339a20a53052bd5f2b2e8438b3c95c91013f653ee781a67934cd1f9f9631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:23:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:23:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:23:52 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:24:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 07 Dec 2022 02:24:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:24:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:07:55 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Tue, 17 Jan 2023 21:07:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:08:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:08:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:08:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Tue, 17 Jan 2023 21:08:41 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:08:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:08:42 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:08:43 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:08:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9d8a3567e30df99576e0a4dbca773af581230fee203891610e6ccbdaa823d2`  
		Last Modified: Wed, 07 Dec 2022 02:26:00 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1f0f349e08af59ed77c7d56ede70f0c5739daa2477ef54a4ee457f5e3e47`  
		Last Modified: Wed, 07 Dec 2022 02:26:01 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff8dfb9b12b027c35d779fe4f06a9b3d0d26efed52153324cfa2f409423b0d`  
		Last Modified: Wed, 07 Dec 2022 02:25:59 GMT  
		Size: 4.5 MB (4539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56cbebc916d35659623816867a456610961f77db6d9753e738c5564651dfa0`  
		Last Modified: Wed, 07 Dec 2022 02:25:58 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7bdfff0f5b940a8450ad5ef0f25d73f40cc8cc13627bda09a9586e81b74502`  
		Last Modified: Tue, 17 Jan 2023 21:10:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7677d20b791d5ee29bf70cce20582fa06c3634201945e98b8501f20a5f9f0da`  
		Last Modified: Tue, 17 Jan 2023 21:10:58 GMT  
		Size: 25.5 MB (25532144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bcfc1167c2472c268123c91440454fe1d68088dce3be90dae9b1fdf1080640`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c0b71b700b5f8b16e6ac83e1bb437b60e10229f74fbc58518cc4c621cf61`  
		Last Modified: Tue, 17 Jan 2023 21:11:03 GMT  
		Size: 48.4 MB (48449762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa2e026ac3ff90ad7fe835692787abbda5ed6bd469edfa416b1c42f331f78f`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b784fa66c50879ee479e3153e735b274ebd3be28d34000d375ef2462f668446`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:f04fc2e2f01e65d6e2828b4cce2c4761d9258aee71d989e273b2ae309f44a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:8dae5a91219c1789ba43690412f6319ae96f51d8787ce81f820907bff6e6c786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129279340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982339a20a53052bd5f2b2e8438b3c95c91013f653ee781a67934cd1f9f9631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:23:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:23:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:23:52 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:24:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 07 Dec 2022 02:24:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:24:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:07:55 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Tue, 17 Jan 2023 21:07:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:08:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:08:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:08:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Tue, 17 Jan 2023 21:08:41 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:08:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:08:42 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:08:43 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:08:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9d8a3567e30df99576e0a4dbca773af581230fee203891610e6ccbdaa823d2`  
		Last Modified: Wed, 07 Dec 2022 02:26:00 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1f0f349e08af59ed77c7d56ede70f0c5739daa2477ef54a4ee457f5e3e47`  
		Last Modified: Wed, 07 Dec 2022 02:26:01 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff8dfb9b12b027c35d779fe4f06a9b3d0d26efed52153324cfa2f409423b0d`  
		Last Modified: Wed, 07 Dec 2022 02:25:59 GMT  
		Size: 4.5 MB (4539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56cbebc916d35659623816867a456610961f77db6d9753e738c5564651dfa0`  
		Last Modified: Wed, 07 Dec 2022 02:25:58 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7bdfff0f5b940a8450ad5ef0f25d73f40cc8cc13627bda09a9586e81b74502`  
		Last Modified: Tue, 17 Jan 2023 21:10:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7677d20b791d5ee29bf70cce20582fa06c3634201945e98b8501f20a5f9f0da`  
		Last Modified: Tue, 17 Jan 2023 21:10:58 GMT  
		Size: 25.5 MB (25532144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bcfc1167c2472c268123c91440454fe1d68088dce3be90dae9b1fdf1080640`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c0b71b700b5f8b16e6ac83e1bb437b60e10229f74fbc58518cc4c621cf61`  
		Last Modified: Tue, 17 Jan 2023 21:11:03 GMT  
		Size: 48.4 MB (48449762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa2e026ac3ff90ad7fe835692787abbda5ed6bd469edfa416b1c42f331f78f`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b784fa66c50879ee479e3153e735b274ebd3be28d34000d375ef2462f668446`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-debian`

```console
$ docker pull mysql@sha256:6f4fb1b8c2717cbe709e755f83a3d6f52dabe58902569bdaa14d0cc9d4c18d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-debian` - linux; amd64

```console
$ docker pull mysql@sha256:603b9b890043bd774c673060292c818e771135c51d0d2b8b7873151906610220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162644100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4726a7600c6f5c8b58d26e8a5634a13bdff727ee29eebe5edbf9ebdd00533898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:20:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:20:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:20:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:20:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:20:36 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:08:53 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Tue, 17 Jan 2023 21:08:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:09:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:09:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:09:17 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:09:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:09:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:09:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702e45a0d0fab46740d0cf404969001dc0537dd564973fa6f31da2a00cfe5ef8`  
		Last Modified: Wed, 11 Jan 2023 06:22:03 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad96d17a23a7cff619709675f8981274e6a4ff7a9fb99590f0a837511e69a50b`  
		Last Modified: Wed, 11 Jan 2023 06:22:03 GMT  
		Size: 4.2 MB (4182274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1832d5509d3dce5314c5ffb58ac35ef7e35c396457e6fab747267312751708cf`  
		Last Modified: Wed, 11 Jan 2023 06:22:02 GMT  
		Size: 1.4 MB (1388883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a580bc4aa47839f3f325b0a7bd7f927d8f41bb947a8e6d1847048a16c88dc`  
		Last Modified: Wed, 11 Jan 2023 06:22:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562f0a131c6cc56e3a6b85245641c4251cb4bc5e5b97f08d5d97209b8c11c38c`  
		Last Modified: Wed, 11 Jan 2023 06:22:04 GMT  
		Size: 14.1 MB (14089400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5760997e25e0fd516f2aab1a32be22ae0a919faa2c2dd36a3ad098d772ca3495`  
		Last Modified: Wed, 11 Jan 2023 06:22:00 GMT  
		Size: 2.5 KB (2543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2459447ebb40538b162dbc50dd435551e3c63d290fc1fb37555ee724a56989a9`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b7ab69b071a7139fbe466170a22caead38334834a792630c6a0e9b12f15ef6`  
		Last Modified: Tue, 17 Jan 2023 21:11:37 GMT  
		Size: 115.8 MB (115832999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aad2d01a4e6a079bc797ac021db4938622225182fa24eab797ee661d30134e9`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d70cf470197d6c4c9c3f0789a15440b5439ac8536ea8db923608b24b7dfc59`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7-oracle`

```console
$ docker pull mysql@sha256:f04fc2e2f01e65d6e2828b4cce2c4761d9258aee71d989e273b2ae309f44a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8dae5a91219c1789ba43690412f6319ae96f51d8787ce81f820907bff6e6c786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129279340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982339a20a53052bd5f2b2e8438b3c95c91013f653ee781a67934cd1f9f9631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:23:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:23:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:23:52 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:24:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 07 Dec 2022 02:24:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:24:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:07:55 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Tue, 17 Jan 2023 21:07:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:08:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:08:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:08:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Tue, 17 Jan 2023 21:08:41 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:08:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:08:42 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:08:43 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:08:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9d8a3567e30df99576e0a4dbca773af581230fee203891610e6ccbdaa823d2`  
		Last Modified: Wed, 07 Dec 2022 02:26:00 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1f0f349e08af59ed77c7d56ede70f0c5739daa2477ef54a4ee457f5e3e47`  
		Last Modified: Wed, 07 Dec 2022 02:26:01 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff8dfb9b12b027c35d779fe4f06a9b3d0d26efed52153324cfa2f409423b0d`  
		Last Modified: Wed, 07 Dec 2022 02:25:59 GMT  
		Size: 4.5 MB (4539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56cbebc916d35659623816867a456610961f77db6d9753e738c5564651dfa0`  
		Last Modified: Wed, 07 Dec 2022 02:25:58 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7bdfff0f5b940a8450ad5ef0f25d73f40cc8cc13627bda09a9586e81b74502`  
		Last Modified: Tue, 17 Jan 2023 21:10:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7677d20b791d5ee29bf70cce20582fa06c3634201945e98b8501f20a5f9f0da`  
		Last Modified: Tue, 17 Jan 2023 21:10:58 GMT  
		Size: 25.5 MB (25532144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bcfc1167c2472c268123c91440454fe1d68088dce3be90dae9b1fdf1080640`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c0b71b700b5f8b16e6ac83e1bb437b60e10229f74fbc58518cc4c621cf61`  
		Last Modified: Tue, 17 Jan 2023 21:11:03 GMT  
		Size: 48.4 MB (48449762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa2e026ac3ff90ad7fe835692787abbda5ed6bd469edfa416b1c42f331f78f`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b784fa66c50879ee479e3153e735b274ebd3be28d34000d375ef2462f668446`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41`

```console
$ docker pull mysql@sha256:f04fc2e2f01e65d6e2828b4cce2c4761d9258aee71d989e273b2ae309f44a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41` - linux; amd64

```console
$ docker pull mysql@sha256:8dae5a91219c1789ba43690412f6319ae96f51d8787ce81f820907bff6e6c786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129279340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982339a20a53052bd5f2b2e8438b3c95c91013f653ee781a67934cd1f9f9631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:23:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:23:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:23:52 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:24:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 07 Dec 2022 02:24:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:24:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:07:55 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Tue, 17 Jan 2023 21:07:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:08:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:08:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:08:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Tue, 17 Jan 2023 21:08:41 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:08:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:08:42 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:08:43 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:08:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9d8a3567e30df99576e0a4dbca773af581230fee203891610e6ccbdaa823d2`  
		Last Modified: Wed, 07 Dec 2022 02:26:00 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1f0f349e08af59ed77c7d56ede70f0c5739daa2477ef54a4ee457f5e3e47`  
		Last Modified: Wed, 07 Dec 2022 02:26:01 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff8dfb9b12b027c35d779fe4f06a9b3d0d26efed52153324cfa2f409423b0d`  
		Last Modified: Wed, 07 Dec 2022 02:25:59 GMT  
		Size: 4.5 MB (4539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56cbebc916d35659623816867a456610961f77db6d9753e738c5564651dfa0`  
		Last Modified: Wed, 07 Dec 2022 02:25:58 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7bdfff0f5b940a8450ad5ef0f25d73f40cc8cc13627bda09a9586e81b74502`  
		Last Modified: Tue, 17 Jan 2023 21:10:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7677d20b791d5ee29bf70cce20582fa06c3634201945e98b8501f20a5f9f0da`  
		Last Modified: Tue, 17 Jan 2023 21:10:58 GMT  
		Size: 25.5 MB (25532144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bcfc1167c2472c268123c91440454fe1d68088dce3be90dae9b1fdf1080640`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c0b71b700b5f8b16e6ac83e1bb437b60e10229f74fbc58518cc4c621cf61`  
		Last Modified: Tue, 17 Jan 2023 21:11:03 GMT  
		Size: 48.4 MB (48449762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa2e026ac3ff90ad7fe835692787abbda5ed6bd469edfa416b1c42f331f78f`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b784fa66c50879ee479e3153e735b274ebd3be28d34000d375ef2462f668446`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-debian`

```console
$ docker pull mysql@sha256:6f4fb1b8c2717cbe709e755f83a3d6f52dabe58902569bdaa14d0cc9d4c18d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:603b9b890043bd774c673060292c818e771135c51d0d2b8b7873151906610220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162644100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4726a7600c6f5c8b58d26e8a5634a13bdff727ee29eebe5edbf9ebdd00533898`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:20:12 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:20:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:20:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:20:27 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:20:28 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:20:36 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:20:36 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:08:53 GMT
ENV MYSQL_VERSION=5.7.41-1debian10
# Tue, 17 Jan 2023 21:08:54 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:09:16 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:09:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:09:17 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:09:17 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:09:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:09:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702e45a0d0fab46740d0cf404969001dc0537dd564973fa6f31da2a00cfe5ef8`  
		Last Modified: Wed, 11 Jan 2023 06:22:03 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad96d17a23a7cff619709675f8981274e6a4ff7a9fb99590f0a837511e69a50b`  
		Last Modified: Wed, 11 Jan 2023 06:22:03 GMT  
		Size: 4.2 MB (4182274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1832d5509d3dce5314c5ffb58ac35ef7e35c396457e6fab747267312751708cf`  
		Last Modified: Wed, 11 Jan 2023 06:22:02 GMT  
		Size: 1.4 MB (1388883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5a580bc4aa47839f3f325b0a7bd7f927d8f41bb947a8e6d1847048a16c88dc`  
		Last Modified: Wed, 11 Jan 2023 06:22:01 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562f0a131c6cc56e3a6b85245641c4251cb4bc5e5b97f08d5d97209b8c11c38c`  
		Last Modified: Wed, 11 Jan 2023 06:22:04 GMT  
		Size: 14.1 MB (14089400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5760997e25e0fd516f2aab1a32be22ae0a919faa2c2dd36a3ad098d772ca3495`  
		Last Modified: Wed, 11 Jan 2023 06:22:00 GMT  
		Size: 2.5 KB (2543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2459447ebb40538b162dbc50dd435551e3c63d290fc1fb37555ee724a56989a9`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b7ab69b071a7139fbe466170a22caead38334834a792630c6a0e9b12f15ef6`  
		Last Modified: Tue, 17 Jan 2023 21:11:37 GMT  
		Size: 115.8 MB (115832999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aad2d01a4e6a079bc797ac021db4938622225182fa24eab797ee661d30134e9`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 5.4 KB (5388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d70cf470197d6c4c9c3f0789a15440b5439ac8536ea8db923608b24b7dfc59`  
		Last Modified: Tue, 17 Jan 2023 21:11:22 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.41-oracle`

```console
$ docker pull mysql@sha256:f04fc2e2f01e65d6e2828b4cce2c4761d9258aee71d989e273b2ae309f44a945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8dae5a91219c1789ba43690412f6319ae96f51d8787ce81f820907bff6e6c786
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.3 MB (129279340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e982339a20a53052bd5f2b2e8438b3c95c91013f653ee781a67934cd1f9f9631`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:56 GMT
ADD file:3853624d773c4bf6fc1464ca06bd07366109fab78072fcab59075073a5da6525 in / 
# Wed, 07 Dec 2022 01:51:56 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:23:50 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:23:50 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:23:52 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:24:09 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False oracle-epel-release-el7; 	yum install -y --setopt=skip_missing_names_on_install=False 		bzip2 		gzip 		openssl 		xz 		zstd 	; 	yum clean all
# Wed, 07 Dec 2022 02:24:10 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:24:10 GMT
ENV MYSQL_MAJOR=5.7
# Tue, 17 Jan 2023 21:07:55 GMT
ENV MYSQL_VERSION=5.7.41-1.el7
# Tue, 17 Jan 2023 21:07:56 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql5.7-server-minimal]'; 		echo 'name=MySQL 5.7 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-5.7-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:08:15 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-community-server-minimal-$MYSQL_VERSION"; 	yum clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	{ echo '!includedir /etc/mysql/mysql.conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/mysql.conf.d; 		find /etc/my.cnf /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/'; 		mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:08:16 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:08:16 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el7
# Tue, 17 Jan 2023 21:08:41 GMT
RUN set -eux; 	yum install -y --setopt=skip_missing_names_on_install=False "mysql-shell-$MYSQL_SHELL_VERSION"; 	yum clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:08:42 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:08:42 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:08:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:08:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:08:43 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:08:43 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:d26998a7c52d2b84e7927f97651d1d703a805c8e4d3f658a03138721f5a5dd44`  
		Last Modified: Wed, 07 Dec 2022 01:53:46 GMT  
		Size: 49.8 MB (49818482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9d8a3567e30df99576e0a4dbca773af581230fee203891610e6ccbdaa823d2`  
		Last Modified: Wed, 07 Dec 2022 02:26:00 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfee1f0f349e08af59ed77c7d56ede70f0c5739daa2477ef54a4ee457f5e3e47`  
		Last Modified: Wed, 07 Dec 2022 02:26:01 GMT  
		Size: 930.2 KB (930227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71ff8dfb9b12b027c35d779fe4f06a9b3d0d26efed52153324cfa2f409423b0d`  
		Last Modified: Wed, 07 Dec 2022 02:25:59 GMT  
		Size: 4.5 MB (4539026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56cbebc916d35659623816867a456610961f77db6d9753e738c5564651dfa0`  
		Last Modified: Wed, 07 Dec 2022 02:25:58 GMT  
		Size: 2.7 KB (2658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7bdfff0f5b940a8450ad5ef0f25d73f40cc8cc13627bda09a9586e81b74502`  
		Last Modified: Tue, 17 Jan 2023 21:10:56 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7677d20b791d5ee29bf70cce20582fa06c3634201945e98b8501f20a5f9f0da`  
		Last Modified: Tue, 17 Jan 2023 21:10:58 GMT  
		Size: 25.5 MB (25532144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4bcfc1167c2472c268123c91440454fe1d68088dce3be90dae9b1fdf1080640`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 320.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f1c0b71b700b5f8b16e6ac83e1bb437b60e10229f74fbc58518cc4c621cf61`  
		Last Modified: Tue, 17 Jan 2023 21:11:03 GMT  
		Size: 48.4 MB (48449762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aa2e026ac3ff90ad7fe835692787abbda5ed6bd469edfa416b1c42f331f78f`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b784fa66c50879ee479e3153e735b274ebd3be28d34000d375ef2462f668446`  
		Last Modified: Tue, 17 Jan 2023 21:10:54 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-debian`

```console
$ docker pull mysql@sha256:36a7e9407344cd1cb4064179962c207cd2afb13bfbb63992f0ca328e4b56b515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c86f3664bddd89bd539049f71c1ffc0816e18d01fad192addfb02d9e2834351c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177699276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba092bab95e48e4e7ea71d2f5e5603108185e259e011179aa03b26ad5d5067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:19:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:19:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:19:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:07:31 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Tue, 17 Jan 2023 21:07:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:07:48 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:07:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:49 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Jan 2023 21:07:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:50 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d346580bcb1a6e9e1becd3883a38670cdca1f47b7cdbe65121708af5458a0318`  
		Last Modified: Wed, 11 Jan 2023 06:21:26 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec40bb6547aaa95db6bda6d1de84761264c716477d2d8b998856586285b4ec55`  
		Last Modified: Wed, 11 Jan 2023 06:21:27 GMT  
		Size: 4.4 MB (4414919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efef7c7e25176536d7c2c61700c323a83aa93894c4e3f250e6318cc77182410c`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 1.4 MB (1418481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd4a9c65ce2ab7c83d934277938ac0b60b14038ed82a23768c5829e04bca7f`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4caf695f1e31c50fb977d1da7e28a7de9f4dacc6d937f16b3b2da8b263527ab`  
		Last Modified: Wed, 11 Jan 2023 06:21:28 GMT  
		Size: 12.7 MB (12662003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621837b69253e21538e7e8b097d99a96bbd14ef7c98668c7f1587a5898849f36`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50c903d5cfd80f351193456503656367928154b4d6c52beb99423204b56df74`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406689e3dbcc29124df7a749b01725da213b58aea774407bdb102b0d00567b4a`  
		Last Modified: Tue, 17 Jan 2023 21:10:40 GMT  
		Size: 127.8 MB (127795859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016832f0b21d3dbdb52cbe137c71f532d7f4515eb11a6d50e6590a5621cef82`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4236ef87c29f872eca03df1e079fbb2b174c44258b1ac06d6ccbd10a7c7efc`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedfbe312f9b4e2371da8769a8336c98cc9639575b92216f327fa63b4d034558`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:36a7e9407344cd1cb4064179962c207cd2afb13bfbb63992f0ca328e4b56b515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c86f3664bddd89bd539049f71c1ffc0816e18d01fad192addfb02d9e2834351c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177699276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba092bab95e48e4e7ea71d2f5e5603108185e259e011179aa03b26ad5d5067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:19:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:19:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:19:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:07:31 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Tue, 17 Jan 2023 21:07:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:07:48 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:07:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:49 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Jan 2023 21:07:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:50 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d346580bcb1a6e9e1becd3883a38670cdca1f47b7cdbe65121708af5458a0318`  
		Last Modified: Wed, 11 Jan 2023 06:21:26 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec40bb6547aaa95db6bda6d1de84761264c716477d2d8b998856586285b4ec55`  
		Last Modified: Wed, 11 Jan 2023 06:21:27 GMT  
		Size: 4.4 MB (4414919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efef7c7e25176536d7c2c61700c323a83aa93894c4e3f250e6318cc77182410c`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 1.4 MB (1418481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd4a9c65ce2ab7c83d934277938ac0b60b14038ed82a23768c5829e04bca7f`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4caf695f1e31c50fb977d1da7e28a7de9f4dacc6d937f16b3b2da8b263527ab`  
		Last Modified: Wed, 11 Jan 2023 06:21:28 GMT  
		Size: 12.7 MB (12662003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621837b69253e21538e7e8b097d99a96bbd14ef7c98668c7f1587a5898849f36`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50c903d5cfd80f351193456503656367928154b4d6c52beb99423204b56df74`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406689e3dbcc29124df7a749b01725da213b58aea774407bdb102b0d00567b4a`  
		Last Modified: Tue, 17 Jan 2023 21:10:40 GMT  
		Size: 127.8 MB (127795859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016832f0b21d3dbdb52cbe137c71f532d7f4515eb11a6d50e6590a5621cef82`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4236ef87c29f872eca03df1e079fbb2b174c44258b1ac06d6ccbd10a7c7efc`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedfbe312f9b4e2371da8769a8336c98cc9639575b92216f327fa63b4d034558`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-debian`

```console
$ docker pull mysql@sha256:36a7e9407344cd1cb4064179962c207cd2afb13bfbb63992f0ca328e4b56b515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.32-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c86f3664bddd89bd539049f71c1ffc0816e18d01fad192addfb02d9e2834351c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177699276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba092bab95e48e4e7ea71d2f5e5603108185e259e011179aa03b26ad5d5067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:19:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:19:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:19:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:07:31 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Tue, 17 Jan 2023 21:07:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:07:48 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:07:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:49 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Jan 2023 21:07:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:50 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d346580bcb1a6e9e1becd3883a38670cdca1f47b7cdbe65121708af5458a0318`  
		Last Modified: Wed, 11 Jan 2023 06:21:26 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec40bb6547aaa95db6bda6d1de84761264c716477d2d8b998856586285b4ec55`  
		Last Modified: Wed, 11 Jan 2023 06:21:27 GMT  
		Size: 4.4 MB (4414919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efef7c7e25176536d7c2c61700c323a83aa93894c4e3f250e6318cc77182410c`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 1.4 MB (1418481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd4a9c65ce2ab7c83d934277938ac0b60b14038ed82a23768c5829e04bca7f`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4caf695f1e31c50fb977d1da7e28a7de9f4dacc6d937f16b3b2da8b263527ab`  
		Last Modified: Wed, 11 Jan 2023 06:21:28 GMT  
		Size: 12.7 MB (12662003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621837b69253e21538e7e8b097d99a96bbd14ef7c98668c7f1587a5898849f36`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50c903d5cfd80f351193456503656367928154b4d6c52beb99423204b56df74`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406689e3dbcc29124df7a749b01725da213b58aea774407bdb102b0d00567b4a`  
		Last Modified: Tue, 17 Jan 2023 21:10:40 GMT  
		Size: 127.8 MB (127795859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016832f0b21d3dbdb52cbe137c71f532d7f4515eb11a6d50e6590a5621cef82`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4236ef87c29f872eca03df1e079fbb2b174c44258b1ac06d6ccbd10a7c7efc`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedfbe312f9b4e2371da8769a8336c98cc9639575b92216f327fa63b4d034558`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.32-oracle`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:8.0.32-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:8.0.32-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:debian`

```console
$ docker pull mysql@sha256:36a7e9407344cd1cb4064179962c207cd2afb13bfbb63992f0ca328e4b56b515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:debian` - linux; amd64

```console
$ docker pull mysql@sha256:c86f3664bddd89bd539049f71c1ffc0816e18d01fad192addfb02d9e2834351c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177699276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ba092bab95e48e4e7ea71d2f5e5603108185e259e011179aa03b26ad5d5067`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 06:19:22 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Wed, 11 Jan 2023 06:19:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:28 GMT
ENV GOSU_VERSION=1.14
# Wed, 11 Jan 2023 06:19:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 11 Jan 2023 06:19:38 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Wed, 11 Jan 2023 06:19:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 06:19:45 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"
# Wed, 11 Jan 2023 06:19:45 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:07:31 GMT
ENV MYSQL_VERSION=8.0.32-1debian11
# Tue, 17 Jan 2023 21:07:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bullseye mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Tue, 17 Jan 2023 21:07:48 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 17 Jan 2023 21:07:49 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:49 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Tue, 17 Jan 2023 21:07:49 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:50 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:50 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:50 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d346580bcb1a6e9e1becd3883a38670cdca1f47b7cdbe65121708af5458a0318`  
		Last Modified: Wed, 11 Jan 2023 06:21:26 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec40bb6547aaa95db6bda6d1de84761264c716477d2d8b998856586285b4ec55`  
		Last Modified: Wed, 11 Jan 2023 06:21:27 GMT  
		Size: 4.4 MB (4414919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efef7c7e25176536d7c2c61700c323a83aa93894c4e3f250e6318cc77182410c`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 1.4 MB (1418481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8cd4a9c65ce2ab7c83d934277938ac0b60b14038ed82a23768c5829e04bca7f`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4caf695f1e31c50fb977d1da7e28a7de9f4dacc6d937f16b3b2da8b263527ab`  
		Last Modified: Wed, 11 Jan 2023 06:21:28 GMT  
		Size: 12.7 MB (12662003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621837b69253e21538e7e8b097d99a96bbd14ef7c98668c7f1587a5898849f36`  
		Last Modified: Wed, 11 Jan 2023 06:21:25 GMT  
		Size: 2.5 KB (2546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50c903d5cfd80f351193456503656367928154b4d6c52beb99423204b56df74`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406689e3dbcc29124df7a749b01725da213b58aea774407bdb102b0d00567b4a`  
		Last Modified: Tue, 17 Jan 2023 21:10:40 GMT  
		Size: 127.8 MB (127795859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4016832f0b21d3dbdb52cbe137c71f532d7f4515eb11a6d50e6590a5621cef82`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4236ef87c29f872eca03df1e079fbb2b174c44258b1ac06d6ccbd10a7c7efc`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedfbe312f9b4e2371da8769a8336c98cc9639575b92216f327fa63b4d034558`  
		Last Modified: Tue, 17 Jan 2023 21:10:20 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:oracle`

```console
$ docker pull mysql@sha256:f451d12bbfe17bb9866b42a74c0df5898e1812260b2a95ad91d86c0e111fe5fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f287894fec0829612a3e921fbc849c0fb0f48356e0ade1e30a790e119274db61
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151967668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde6c84943bbf34dfa9ea6bd491ef95a049c41a6fc2a9ea0bc36134b1b093860`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 01:51:27 GMT
ADD file:04d9ae26c2acac414b69a784563f765d531aeaf941ea0341025b4544f9ade244 in / 
# Wed, 07 Dec 2022 01:51:27 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:21:54 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:21:55 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:21:58 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:22:21 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:22:22 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:22:23 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:06:08 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:06:09 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:06:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:06:42 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:06:42 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:07:17 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:07:17 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:07:18 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:07:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:07:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:07:18 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:07:18 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:0ed027b72ddc5d1a749fc58b7c26610167393b08ae71ef6625496508903f70a2`  
		Last Modified: Wed, 07 Dec 2022 01:53:11 GMT  
		Size: 43.9 MB (43868738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0296159747f12f208fbf9721970ca290348698ac443cf98311477b6e44f18acc`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 886.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2f9b664bd354b5b8823bbdda42cf0813f2d8d3b5693f952c0a8516af84a826`  
		Last Modified: Wed, 07 Dec 2022 02:25:25 GMT  
		Size: 928.8 KB (928835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6519f81c2689152b478834162cfe2f21ef37c472108a3e3a03a6ac0f5cbdd9`  
		Last Modified: Wed, 07 Dec 2022 02:25:24 GMT  
		Size: 4.6 MB (4608004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36bb5e56d458a7652c87ab8c3909c0ad098feaa81e73649bb37704701ca3ee6d`  
		Last Modified: Wed, 07 Dec 2022 02:25:23 GMT  
		Size: 2.6 KB (2630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810ed59509062a1c771f01b920f00fca2b3a126e561355506188bdc924e65c0`  
		Last Modified: Tue, 17 Jan 2023 21:09:47 GMT  
		Size: 336.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:788d365517771ca199779a25f2faf5c1d75408f7e57cd0e6bdd34181b9ec720d`  
		Last Modified: Tue, 17 Jan 2023 21:09:53 GMT  
		Size: 56.2 MB (56220298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13d785f9637b9cdede74b0f332edd33b652fe329dbba2ff0e27388af786fc23`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75755e293f40636019b4c1c800464f9e4969f3bbb0920be3f77c31b5c22796f4`  
		Last Modified: Tue, 17 Jan 2023 21:09:54 GMT  
		Size: 46.3 MB (46332108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00b9182546d2f7832e16d2f174914a30f32048a2cb313a889e774bcaeb2f0c8`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 5.4 KB (5393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0145b16e9f9ed8b2695da8098729f6337a67c57d2853d9edbcb4caab78b99`  
		Last Modified: Tue, 17 Jan 2023 21:09:45 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8a7599f63dda9798f0eb1c6a4d813eebab2f8137a0fcc5ab97cadaa0bcffc42c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150880296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07039bb92a6f9fe85e7d50648e3d0bdab8504f1b25ceed88157bf3dd843fe009`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 07 Dec 2022 02:10:44 GMT
ADD file:6fdd782c2779edf7149126e79dcb46ebde32975107cdd5d129cce0860e797cde in / 
# Wed, 07 Dec 2022 02:10:44 GMT
CMD ["/bin/bash"]
# Wed, 07 Dec 2022 02:50:18 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql
# Wed, 07 Dec 2022 02:50:18 GMT
ENV GOSU_VERSION=1.14
# Wed, 07 Dec 2022 02:50:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 07 Dec 2022 02:50:43 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all
# Wed, 07 Dec 2022 02:50:44 GMT
RUN set -eux; 	key='859BE8D7C586F538430B19C2467B942D3A79BD29'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME"
# Wed, 07 Dec 2022 02:50:44 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 17 Jan 2023 21:15:43 GMT
ENV MYSQL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:15:44 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo
# Tue, 17 Jan 2023 21:16:12 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version
# Tue, 17 Jan 2023 21:16:13 GMT
RUN set -eu; 	. /etc/os-release; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo "baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/${VERSION_ID%%[.-]*}/\$basearch/"; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo
# Tue, 17 Jan 2023 21:16:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.32-1.el8
# Tue, 17 Jan 2023 21:16:45 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version
# Tue, 17 Jan 2023 21:16:46 GMT
VOLUME [/var/lib/mysql]
# Tue, 17 Jan 2023 21:16:47 GMT
COPY file:e9c22353a1133b89c5bca24ecacd348acd094e50e5e5c45375a997c6b1f07192 in /usr/local/bin/ 
# Tue, 17 Jan 2023 21:16:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 17 Jan 2023 21:16:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 17 Jan 2023 21:16:47 GMT
EXPOSE 3306 33060
# Tue, 17 Jan 2023 21:16:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:12a06ca91af857ea3cb02aedc5c643c5f06865868ae5c386c8ea664be60ead7e`  
		Last Modified: Wed, 07 Dec 2022 02:12:09 GMT  
		Size: 42.8 MB (42772059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fec1cb1944f64443d61a29e94cddba36d0cb8a09c80e0247375445bc62b842e`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aede38c79379349fd3e9d191f92be36e68adc230840ae21c015f166b96e2067a`  
		Last Modified: Wed, 07 Dec 2022 02:52:10 GMT  
		Size: 857.2 KB (857168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51b980849561d1ed6bffe5deb621498e150f4f0f148af7a2654dd90ed42d7bfb`  
		Last Modified: Wed, 07 Dec 2022 02:52:09 GMT  
		Size: 4.5 MB (4464908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f503d79ed4bc3c439b28068291b1260757ab2de86163c8954962d88ff917e22a`  
		Last Modified: Wed, 07 Dec 2022 02:52:08 GMT  
		Size: 2.6 KB (2624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68c2b43a7e4bae0b356fff0c9bc14905bd8d305d062cb4ea5d1c2275a4c39273`  
		Last Modified: Tue, 17 Jan 2023 21:17:06 GMT  
		Size: 338.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2bb95bebe3faba3509fb704207e81b5c81c2831256fa63f314d15a5e7513f`  
		Last Modified: Tue, 17 Jan 2023 21:17:13 GMT  
		Size: 55.6 MB (55610757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78004d73f3aef777892e3870fc76db5b6a7f7b33c313aedf7a6b873911d41c9`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 319.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871208cde4a40b9f8a4a07d620ac334441848d9ec993bd7fabc452cba1595116`  
		Last Modified: Tue, 17 Jan 2023 21:17:11 GMT  
		Size: 47.2 MB (47165727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4ffd21fbf398e2c8ee0fdee514c745b169697ed03a5eeb632d6cd573b6de66`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 5.4 KB (5390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a2fd13901dca583f16c51f1a7d094bd0b629d231e5cc8b1781fdfd9e61c1e7`  
		Last Modified: Tue, 17 Jan 2023 21:17:04 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
