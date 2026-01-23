## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:6b18d01fb632c0f568ace1cc1ebffb42d1d21bc1de86f6d3e8b7eb18278444d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:c3e237135a7c00c260b63e0bed304a773fdde2dfb8a0b3b96604ce92d5a27500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266380022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aa51c1d154ae3b24b50ea5d03f4e7b1de32d1b47faebc8c94f17d396eee82ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:58:01 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:58:01 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:03:05 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:03:07 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:03:07 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:03:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:03:30 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:03:30 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:55 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:33 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:33 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:33 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:16506d4b4233ebc21b62f7593851ebfe31dec192fdb790c8c857eca6260f7a57`  
		Last Modified: Fri, 23 Jan 2026 00:58:12 GMT  
		Size: 47.3 MB (47313548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fad6da9c39ef2d01593237f9ffcc86e0cefb5510ef65594caa4ea452f69b50`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db79435343ee9d2ddceb00b95c6e68c4b76546fd757c497e65091e72f2f0701`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 783.6 KB (783563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b475ac15d75a4a1bfef7555b1dfc13bc61e282ab16c3ed91015ec337b22c4`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 6.2 MB (6173912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b639f2fb9b22d8d39f193d2a1b33126428f2509f7f64ca4bbc59a10cbfb71509`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63365c83edc90c4fee3b852a42e14f6ac5df8c20e220ea401db3d98651b8318`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e06f1f9481988d7bc98b82647062710771c1386a2c8d694de5cdd5e3d2428d8`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 51.5 MB (51458291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfd97e63adb9eccad66fb09057b1a0c011d52f6ee6bfbb117789378c69a0c77`  
		Last Modified: Fri, 23 Jan 2026 01:05:07 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843ee584592a0505faa7c3f731de8faac61616819a11eb968c7d1021243acb2`  
		Last Modified: Fri, 23 Jan 2026 01:05:11 GMT  
		Size: 160.6 MB (160641216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013be34edccd3ac78d854fe46942a832f6400d1e7cc071bc3ce805048ca471d9`  
		Last Modified: Fri, 23 Jan 2026 01:05:08 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:03440e26447fb275416401f7b8c04131f6a4fa4d7f8e38e5e0fec987a72093ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bfc1ace71370985a5aab72c0c4e78466c26cd2641e618492b19961a5c08bd3`

```dockerfile
```

-	Layers:
	-	`sha256:1fba87b6e331df2af8bdc2f8363613d50e2697c1f7aca599177ca40801e692a5`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 16.3 MB (16297384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d347ea4ed6ece51d08392287f458f2b198ddcf1780b356376db5a60415dee518`  
		Last Modified: Fri, 23 Jan 2026 01:05:06 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:a12f42e2f5b3fc1fc43fa0a0de8bf359ba40cb4fec5d22fb7c82f327e623cafe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261471619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:043282bd532b65463dc2fb9e459831a86573fcf05db16c6b08aceae9951dd524`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 23 Jan 2026 00:57:45 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 23 Jan 2026 00:57:45 GMT
CMD ["/bin/bash"]
# Fri, 23 Jan 2026 01:02:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 23 Jan 2026 01:02:27 GMT
ENV GOSU_VERSION=1.19
# Fri, 23 Jan 2026 01:02:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 23 Jan 2026 01:02:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:02:54 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 23 Jan 2026 01:03:23 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 23 Jan 2026 01:04:05 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
VOLUME [/var/lib/mysql]
# Fri, 23 Jan 2026 01:04:05 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 23 Jan 2026 01:04:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jan 2026 01:04:05 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 23 Jan 2026 01:04:05 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:cb58e3477df4a511e30cc2dda04665dfc7b948e198e587c0ae4203a6cd829165`  
		Last Modified: Fri, 23 Jan 2026 00:57:57 GMT  
		Size: 45.9 MB (45901910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467aafee38032ecf6c7ffdb23fd691160f9e28671fe84d62188aec36b3b2972a`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea485180d0b14e6830854d95412dd474051ecd606e94170908de08f805e6a24`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15698bfe0f53269a1498e220820c702f35251fac2d2fd669a5dcaba68d9362`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 5.8 MB (5793320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:812fc73661ca57f1cf40cdf7c55ccce1f42b3b4fd4ca93b2247c2a8fe0095e50`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a31a1d1ca3093bcbbc2c7631acb6dd8386708446e968255f4a0da9f89cd71fe`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f6e5da3bbe1dd48f44f13cdb8c96f2c47d8ba9b95d3b2ff61c24ff9a9e61f7`  
		Last Modified: Fri, 23 Jan 2026 01:04:44 GMT  
		Size: 50.1 MB (50087651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad2373f3576e76aafd6e63f75eacc6762aad4a290a976fbe6072c8ae20afa26`  
		Last Modified: Fri, 23 Jan 2026 01:04:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda9001891381e69645ba83662f22ce8d03a2a8597bdb9d207d29b008a359f9e`  
		Last Modified: Fri, 23 Jan 2026 01:04:46 GMT  
		Size: 158.9 MB (158941736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a30b55257e3dfdea6a7cbc412be621ccd04b75f3dbf68e9a1a13a7c3ff3cd8c`  
		Last Modified: Fri, 23 Jan 2026 01:04:43 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2331b411cddcfd9e8c10888522a071769640b481f4d6998f2c2997f821be8f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f788f864a54f8e8eacc321cbc9343ed48b5437a274b0ca4aecb8e8af9e0cd00`

```dockerfile
```

-	Layers:
	-	`sha256:606cbf164cc77b3cf5f72d05e460dc8e0c9585dd465866a3d67c3b744fe3ece0`  
		Last Modified: Fri, 23 Jan 2026 01:04:41 GMT  
		Size: 16.3 MB (16295840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:deaa1c79edb77da8e6a7e93b254765326a0bf7fd40518286ee26e0390e438e32`  
		Last Modified: Fri, 23 Jan 2026 01:04:40 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
