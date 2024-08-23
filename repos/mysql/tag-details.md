<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux9`](#mysql8-oraclelinux9)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux9`](#mysql80-oraclelinux9)
-	[`mysql:8.0.39`](#mysql8039)
-	[`mysql:8.0.39-bookworm`](#mysql8039-bookworm)
-	[`mysql:8.0.39-debian`](#mysql8039-debian)
-	[`mysql:8.0.39-oracle`](#mysql8039-oracle)
-	[`mysql:8.0.39-oraclelinux9`](#mysql8039-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.2`](#mysql842)
-	[`mysql:8.4.2-oracle`](#mysql842-oracle)
-	[`mysql:8.4.2-oraclelinux9`](#mysql842-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.0`](#mysql90)
-	[`mysql:9.0-oracle`](#mysql90-oracle)
-	[`mysql:9.0-oraclelinux9`](#mysql90-oraclelinux9)
-	[`mysql:9.0.1`](#mysql901)
-	[`mysql:9.0.1-oracle`](#mysql901-oracle)
-	[`mysql:9.0.1-oraclelinux9`](#mysql901-oraclelinux9)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux9`](#mysqlinnovation-oraclelinux9)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:lts`](#mysqllts)
-	[`mysql:lts-oracle`](#mysqllts-oracle)
-	[`mysql:lts-oraclelinux9`](#mysqllts-oraclelinux9)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux9`](#mysqloraclelinux9)

## `mysql:8`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:c253b12ccf0c8b291af74f49cb7871bd822a0c71fb6d53d2e1c9f21b5f09b2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:0cb3ab06963a548f8eebb5aca9e06a0ea86db8178030f2e12edda36143a41259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167066842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8c3640577ec4c7a337d2376517832100a8df15b898e1cd4556750029804ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501b7dd297efa7df14b181f530712c03e4d07d7392768487270bd4402d4973`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c3c8425aebc06e1bb837ed9c09de67f979e209801f9797172b43c7ac1c374`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e545ccd1cfca01bba9cf729e86d46d7ff2656bc1ed3f94e24cc4fc4ce1613eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.7 MB (6731692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd749ad2b919b92916e0a41d9b266612ccb4ea70c6eaa71d4580b430b5c6a`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85a79daec728d49fdd898382156dc08eb4dadc0be7d9b7191842d9c34d037`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbbbba665339ec8f25cc36dc3158c64b2e11414f723532aff207c9777a78ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 49.2 MB (49178891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1253e3c023cd06fe203f4604165d2359a8d17694f02920ba62f09befbbb6419`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bd751a6d962970ee08cc2419b9a8a5207794cd6dc9584fe7b4f885dcc02a2`  
		Last Modified: Fri, 23 Aug 2024 01:50:59 GMT  
		Size: 60.9 MB (60929605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73384984c3a6f1f6027b09e0be131a98fd3a582b8d64944006d52d2fc33ab5`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e706c318d8c0d30be02562309b3ca1449c94cb7c9bdb6049e0f0e859bad7c3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fdfb587eefe3f939448c40150bd3ca1eacef355be061a97538396da8e1fa5e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13839976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2672e5e37229751c02f34512e9f981a0f5173414e023e1bdf812bfd0027424`

```dockerfile
```

-	Layers:
	-	`sha256:74f136e8de607d9fee65502f44e2769110992dfa06033910c0e6c82000c9172f`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.8 MB (13805195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486712bc68c230afa0305cf4b01c18470d0136ecd5c96910b16d2b81f8a1acaa`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:05343927ef5abe24dc77fa24e42719d1be3aa5c6f18d839cd5733126a581a993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0097b8a9d94b29005a790aba94aff0b3de55ef46e868ba3dc6975c516392d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6119f7988c09f46c88dabc21de5ee71f3037389bf54f65745c144c8981f70`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ffc2a6281d83ada9945b1c2c3ee58e84e40488c95ea612ad24b685c0ef3c3`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 48.1 MB (48056781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20aaad5eace96cf23c69b9bc5216570e66e36e7802208dc836ea51409493344`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f116c04068ffa62559cc40b1164c4443f8a45302338379c3ade4c8a43053ccd`  
		Last Modified: Fri, 23 Aug 2024 01:53:37 GMT  
		Size: 68.4 MB (68421591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdec858f245296d1c7329e536ea978fb1ef04c1683bd433cdd88809bf628b59`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d18518856de073ebf464e4e2698e2a5f2ff4ed863d8ba3283507a61d86ed9`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:38edee0b4107ea4224a6abc79f7b953591b3e5186057fcdc9fb859299ff6244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13835385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4022476141f42ba29d81e8b51fc6177e2b47b33e42636d66ccd321742391f`

```dockerfile
```

-	Layers:
	-	`sha256:026ac9441b137f1469427e14e8ff66b9433da6760407da5a03fa0df832f23044`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 13.8 MB (13800273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f9611fc5d846f7663a5a8e266db59eac25a036223a28ef04f4d500c1f066e`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:9c12124dfa4e396219f92a1753e4789de0da5c9a6ca8e3c5725f318c43ae7faa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:cfc33c00539d57efb8f76192be358cce23a1b3d13e7f8f94d56e446956629fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184745169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f52d1b84a011f46acbdeaf605d3a4d0f113b306ca9759a24aa3e08feb651a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1debian12
# Mon, 22 Jul 2024 22:26:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1a9c2e70996650bd691a61357d027174de2dc392c10cd31b6488223fd4f4e2`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093fc1a24045af4b0d5c98d9f4f2050a74760a68ac45024c68027d12e7b5d60`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.4 MB (4422721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fad174f0a042b8bd9b04778087348e749b9e444f79d4ba8aa0912b0e4d9f45`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.4 MB (1445898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c6e9998aa686af820829f919df26285c31c86c3a9baeafd16e2ec370f921c9`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7459d1296321411777affabf80d090b1fbecc4657eb59595843358339c6312b0`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 15.3 MB (15285512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed7d7067ab8c670931ca8b1189bd9a38826a73bd85738bc7d39984c644130c`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e4d0b6d559dc7e5813daa5608628d05948befcd4a15376cefb2e367a207e28`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73efc838234869d78cc026e990490f94bac9917ef8173cbaa5e779339909fc3b`  
		Last Modified: Tue, 13 Aug 2024 01:20:31 GMT  
		Size: 134.5 MB (134454538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20c1e095b0f267f035dc7e31426a088d74274bd66f91e8111f23ae3df2c7f66`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b38537e038091ed75237387ec86924b0038c6ca335ab6f3e2adfb5275e541c2`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4ec1205180dcf1b27f844ac2b1928ec5a6ce3d38b770e65811b8f53fa3857`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:768063bfdab5099b0fa869f9948135fc4ef46f2460cd231d8c169df32c93203b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e48e9480f68405cadd927fcac632f93919f262e97f4de0c984b2c23004655f4`

```dockerfile
```

-	Layers:
	-	`sha256:35ce39bc321eec5395ba1ee5f11c00221baf5503c2a0d93a22940fe6d1cc47cc`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d962fde7e57bfa50c345f120cf2f1820877b7334b3bc8e17274aa6f2fe8b31`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 34.1 KB (34137 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:9c12124dfa4e396219f92a1753e4789de0da5c9a6ca8e3c5725f318c43ae7faa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cfc33c00539d57efb8f76192be358cce23a1b3d13e7f8f94d56e446956629fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184745169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f52d1b84a011f46acbdeaf605d3a4d0f113b306ca9759a24aa3e08feb651a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1debian12
# Mon, 22 Jul 2024 22:26:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1a9c2e70996650bd691a61357d027174de2dc392c10cd31b6488223fd4f4e2`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093fc1a24045af4b0d5c98d9f4f2050a74760a68ac45024c68027d12e7b5d60`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.4 MB (4422721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fad174f0a042b8bd9b04778087348e749b9e444f79d4ba8aa0912b0e4d9f45`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.4 MB (1445898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c6e9998aa686af820829f919df26285c31c86c3a9baeafd16e2ec370f921c9`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7459d1296321411777affabf80d090b1fbecc4657eb59595843358339c6312b0`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 15.3 MB (15285512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed7d7067ab8c670931ca8b1189bd9a38826a73bd85738bc7d39984c644130c`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e4d0b6d559dc7e5813daa5608628d05948befcd4a15376cefb2e367a207e28`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73efc838234869d78cc026e990490f94bac9917ef8173cbaa5e779339909fc3b`  
		Last Modified: Tue, 13 Aug 2024 01:20:31 GMT  
		Size: 134.5 MB (134454538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20c1e095b0f267f035dc7e31426a088d74274bd66f91e8111f23ae3df2c7f66`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b38537e038091ed75237387ec86924b0038c6ca335ab6f3e2adfb5275e541c2`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4ec1205180dcf1b27f844ac2b1928ec5a6ce3d38b770e65811b8f53fa3857`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:768063bfdab5099b0fa869f9948135fc4ef46f2460cd231d8c169df32c93203b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e48e9480f68405cadd927fcac632f93919f262e97f4de0c984b2c23004655f4`

```dockerfile
```

-	Layers:
	-	`sha256:35ce39bc321eec5395ba1ee5f11c00221baf5503c2a0d93a22940fe6d1cc47cc`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d962fde7e57bfa50c345f120cf2f1820877b7334b3bc8e17274aa6f2fe8b31`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 34.1 KB (34137 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:c253b12ccf0c8b291af74f49cb7871bd822a0c71fb6d53d2e1c9f21b5f09b2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0cb3ab06963a548f8eebb5aca9e06a0ea86db8178030f2e12edda36143a41259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167066842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8c3640577ec4c7a337d2376517832100a8df15b898e1cd4556750029804ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501b7dd297efa7df14b181f530712c03e4d07d7392768487270bd4402d4973`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c3c8425aebc06e1bb837ed9c09de67f979e209801f9797172b43c7ac1c374`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e545ccd1cfca01bba9cf729e86d46d7ff2656bc1ed3f94e24cc4fc4ce1613eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.7 MB (6731692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd749ad2b919b92916e0a41d9b266612ccb4ea70c6eaa71d4580b430b5c6a`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85a79daec728d49fdd898382156dc08eb4dadc0be7d9b7191842d9c34d037`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbbbba665339ec8f25cc36dc3158c64b2e11414f723532aff207c9777a78ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 49.2 MB (49178891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1253e3c023cd06fe203f4604165d2359a8d17694f02920ba62f09befbbb6419`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bd751a6d962970ee08cc2419b9a8a5207794cd6dc9584fe7b4f885dcc02a2`  
		Last Modified: Fri, 23 Aug 2024 01:50:59 GMT  
		Size: 60.9 MB (60929605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73384984c3a6f1f6027b09e0be131a98fd3a582b8d64944006d52d2fc33ab5`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e706c318d8c0d30be02562309b3ca1449c94cb7c9bdb6049e0f0e859bad7c3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fdfb587eefe3f939448c40150bd3ca1eacef355be061a97538396da8e1fa5e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13839976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2672e5e37229751c02f34512e9f981a0f5173414e023e1bdf812bfd0027424`

```dockerfile
```

-	Layers:
	-	`sha256:74f136e8de607d9fee65502f44e2769110992dfa06033910c0e6c82000c9172f`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.8 MB (13805195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486712bc68c230afa0305cf4b01c18470d0136ecd5c96910b16d2b81f8a1acaa`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:05343927ef5abe24dc77fa24e42719d1be3aa5c6f18d839cd5733126a581a993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0097b8a9d94b29005a790aba94aff0b3de55ef46e868ba3dc6975c516392d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6119f7988c09f46c88dabc21de5ee71f3037389bf54f65745c144c8981f70`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ffc2a6281d83ada9945b1c2c3ee58e84e40488c95ea612ad24b685c0ef3c3`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 48.1 MB (48056781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20aaad5eace96cf23c69b9bc5216570e66e36e7802208dc836ea51409493344`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f116c04068ffa62559cc40b1164c4443f8a45302338379c3ade4c8a43053ccd`  
		Last Modified: Fri, 23 Aug 2024 01:53:37 GMT  
		Size: 68.4 MB (68421591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdec858f245296d1c7329e536ea978fb1ef04c1683bd433cdd88809bf628b59`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d18518856de073ebf464e4e2698e2a5f2ff4ed863d8ba3283507a61d86ed9`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:38edee0b4107ea4224a6abc79f7b953591b3e5186057fcdc9fb859299ff6244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13835385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4022476141f42ba29d81e8b51fc6177e2b47b33e42636d66ccd321742391f`

```dockerfile
```

-	Layers:
	-	`sha256:026ac9441b137f1469427e14e8ff66b9433da6760407da5a03fa0df832f23044`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 13.8 MB (13800273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f9611fc5d846f7663a5a8e266db59eac25a036223a28ef04f4d500c1f066e`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c253b12ccf0c8b291af74f49cb7871bd822a0c71fb6d53d2e1c9f21b5f09b2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0cb3ab06963a548f8eebb5aca9e06a0ea86db8178030f2e12edda36143a41259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167066842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8c3640577ec4c7a337d2376517832100a8df15b898e1cd4556750029804ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501b7dd297efa7df14b181f530712c03e4d07d7392768487270bd4402d4973`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c3c8425aebc06e1bb837ed9c09de67f979e209801f9797172b43c7ac1c374`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e545ccd1cfca01bba9cf729e86d46d7ff2656bc1ed3f94e24cc4fc4ce1613eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.7 MB (6731692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd749ad2b919b92916e0a41d9b266612ccb4ea70c6eaa71d4580b430b5c6a`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85a79daec728d49fdd898382156dc08eb4dadc0be7d9b7191842d9c34d037`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbbbba665339ec8f25cc36dc3158c64b2e11414f723532aff207c9777a78ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 49.2 MB (49178891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1253e3c023cd06fe203f4604165d2359a8d17694f02920ba62f09befbbb6419`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bd751a6d962970ee08cc2419b9a8a5207794cd6dc9584fe7b4f885dcc02a2`  
		Last Modified: Fri, 23 Aug 2024 01:50:59 GMT  
		Size: 60.9 MB (60929605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73384984c3a6f1f6027b09e0be131a98fd3a582b8d64944006d52d2fc33ab5`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e706c318d8c0d30be02562309b3ca1449c94cb7c9bdb6049e0f0e859bad7c3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fdfb587eefe3f939448c40150bd3ca1eacef355be061a97538396da8e1fa5e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13839976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2672e5e37229751c02f34512e9f981a0f5173414e023e1bdf812bfd0027424`

```dockerfile
```

-	Layers:
	-	`sha256:74f136e8de607d9fee65502f44e2769110992dfa06033910c0e6c82000c9172f`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.8 MB (13805195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486712bc68c230afa0305cf4b01c18470d0136ecd5c96910b16d2b81f8a1acaa`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:05343927ef5abe24dc77fa24e42719d1be3aa5c6f18d839cd5733126a581a993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0097b8a9d94b29005a790aba94aff0b3de55ef46e868ba3dc6975c516392d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6119f7988c09f46c88dabc21de5ee71f3037389bf54f65745c144c8981f70`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ffc2a6281d83ada9945b1c2c3ee58e84e40488c95ea612ad24b685c0ef3c3`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 48.1 MB (48056781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20aaad5eace96cf23c69b9bc5216570e66e36e7802208dc836ea51409493344`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f116c04068ffa62559cc40b1164c4443f8a45302338379c3ade4c8a43053ccd`  
		Last Modified: Fri, 23 Aug 2024 01:53:37 GMT  
		Size: 68.4 MB (68421591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdec858f245296d1c7329e536ea978fb1ef04c1683bd433cdd88809bf628b59`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d18518856de073ebf464e4e2698e2a5f2ff4ed863d8ba3283507a61d86ed9`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:38edee0b4107ea4224a6abc79f7b953591b3e5186057fcdc9fb859299ff6244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13835385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4022476141f42ba29d81e8b51fc6177e2b47b33e42636d66ccd321742391f`

```dockerfile
```

-	Layers:
	-	`sha256:026ac9441b137f1469427e14e8ff66b9433da6760407da5a03fa0df832f23044`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 13.8 MB (13800273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f9611fc5d846f7663a5a8e266db59eac25a036223a28ef04f4d500c1f066e`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39`

```console
$ docker pull mysql@sha256:c253b12ccf0c8b291af74f49cb7871bd822a0c71fb6d53d2e1c9f21b5f09b2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.39` - linux; amd64

```console
$ docker pull mysql@sha256:0cb3ab06963a548f8eebb5aca9e06a0ea86db8178030f2e12edda36143a41259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167066842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8c3640577ec4c7a337d2376517832100a8df15b898e1cd4556750029804ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501b7dd297efa7df14b181f530712c03e4d07d7392768487270bd4402d4973`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c3c8425aebc06e1bb837ed9c09de67f979e209801f9797172b43c7ac1c374`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e545ccd1cfca01bba9cf729e86d46d7ff2656bc1ed3f94e24cc4fc4ce1613eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.7 MB (6731692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd749ad2b919b92916e0a41d9b266612ccb4ea70c6eaa71d4580b430b5c6a`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85a79daec728d49fdd898382156dc08eb4dadc0be7d9b7191842d9c34d037`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbbbba665339ec8f25cc36dc3158c64b2e11414f723532aff207c9777a78ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 49.2 MB (49178891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1253e3c023cd06fe203f4604165d2359a8d17694f02920ba62f09befbbb6419`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bd751a6d962970ee08cc2419b9a8a5207794cd6dc9584fe7b4f885dcc02a2`  
		Last Modified: Fri, 23 Aug 2024 01:50:59 GMT  
		Size: 60.9 MB (60929605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73384984c3a6f1f6027b09e0be131a98fd3a582b8d64944006d52d2fc33ab5`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e706c318d8c0d30be02562309b3ca1449c94cb7c9bdb6049e0f0e859bad7c3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39` - unknown; unknown

```console
$ docker pull mysql@sha256:fdfb587eefe3f939448c40150bd3ca1eacef355be061a97538396da8e1fa5e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13839976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2672e5e37229751c02f34512e9f981a0f5173414e023e1bdf812bfd0027424`

```dockerfile
```

-	Layers:
	-	`sha256:74f136e8de607d9fee65502f44e2769110992dfa06033910c0e6c82000c9172f`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.8 MB (13805195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486712bc68c230afa0305cf4b01c18470d0136ecd5c96910b16d2b81f8a1acaa`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.39` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:05343927ef5abe24dc77fa24e42719d1be3aa5c6f18d839cd5733126a581a993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0097b8a9d94b29005a790aba94aff0b3de55ef46e868ba3dc6975c516392d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6119f7988c09f46c88dabc21de5ee71f3037389bf54f65745c144c8981f70`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ffc2a6281d83ada9945b1c2c3ee58e84e40488c95ea612ad24b685c0ef3c3`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 48.1 MB (48056781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20aaad5eace96cf23c69b9bc5216570e66e36e7802208dc836ea51409493344`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f116c04068ffa62559cc40b1164c4443f8a45302338379c3ade4c8a43053ccd`  
		Last Modified: Fri, 23 Aug 2024 01:53:37 GMT  
		Size: 68.4 MB (68421591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdec858f245296d1c7329e536ea978fb1ef04c1683bd433cdd88809bf628b59`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d18518856de073ebf464e4e2698e2a5f2ff4ed863d8ba3283507a61d86ed9`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39` - unknown; unknown

```console
$ docker pull mysql@sha256:38edee0b4107ea4224a6abc79f7b953591b3e5186057fcdc9fb859299ff6244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13835385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4022476141f42ba29d81e8b51fc6177e2b47b33e42636d66ccd321742391f`

```dockerfile
```

-	Layers:
	-	`sha256:026ac9441b137f1469427e14e8ff66b9433da6760407da5a03fa0df832f23044`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 13.8 MB (13800273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f9611fc5d846f7663a5a8e266db59eac25a036223a28ef04f4d500c1f066e`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-bookworm`

```console
$ docker pull mysql@sha256:9c12124dfa4e396219f92a1753e4789de0da5c9a6ca8e3c5725f318c43ae7faa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:cfc33c00539d57efb8f76192be358cce23a1b3d13e7f8f94d56e446956629fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184745169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f52d1b84a011f46acbdeaf605d3a4d0f113b306ca9759a24aa3e08feb651a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1debian12
# Mon, 22 Jul 2024 22:26:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1a9c2e70996650bd691a61357d027174de2dc392c10cd31b6488223fd4f4e2`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093fc1a24045af4b0d5c98d9f4f2050a74760a68ac45024c68027d12e7b5d60`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.4 MB (4422721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fad174f0a042b8bd9b04778087348e749b9e444f79d4ba8aa0912b0e4d9f45`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.4 MB (1445898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c6e9998aa686af820829f919df26285c31c86c3a9baeafd16e2ec370f921c9`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7459d1296321411777affabf80d090b1fbecc4657eb59595843358339c6312b0`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 15.3 MB (15285512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed7d7067ab8c670931ca8b1189bd9a38826a73bd85738bc7d39984c644130c`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e4d0b6d559dc7e5813daa5608628d05948befcd4a15376cefb2e367a207e28`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73efc838234869d78cc026e990490f94bac9917ef8173cbaa5e779339909fc3b`  
		Last Modified: Tue, 13 Aug 2024 01:20:31 GMT  
		Size: 134.5 MB (134454538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20c1e095b0f267f035dc7e31426a088d74274bd66f91e8111f23ae3df2c7f66`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b38537e038091ed75237387ec86924b0038c6ca335ab6f3e2adfb5275e541c2`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4ec1205180dcf1b27f844ac2b1928ec5a6ce3d38b770e65811b8f53fa3857`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:768063bfdab5099b0fa869f9948135fc4ef46f2460cd231d8c169df32c93203b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e48e9480f68405cadd927fcac632f93919f262e97f4de0c984b2c23004655f4`

```dockerfile
```

-	Layers:
	-	`sha256:35ce39bc321eec5395ba1ee5f11c00221baf5503c2a0d93a22940fe6d1cc47cc`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d962fde7e57bfa50c345f120cf2f1820877b7334b3bc8e17274aa6f2fe8b31`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 34.1 KB (34137 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-debian`

```console
$ docker pull mysql@sha256:9c12124dfa4e396219f92a1753e4789de0da5c9a6ca8e3c5725f318c43ae7faa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cfc33c00539d57efb8f76192be358cce23a1b3d13e7f8f94d56e446956629fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184745169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094f52d1b84a011f46acbdeaf605d3a4d0f113b306ca9759a24aa3e08feb651a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1debian12
# Mon, 22 Jul 2024 22:26:32 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1a9c2e70996650bd691a61357d027174de2dc392c10cd31b6488223fd4f4e2`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8093fc1a24045af4b0d5c98d9f4f2050a74760a68ac45024c68027d12e7b5d60`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.4 MB (4422721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fad174f0a042b8bd9b04778087348e749b9e444f79d4ba8aa0912b0e4d9f45`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 1.4 MB (1445898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c6e9998aa686af820829f919df26285c31c86c3a9baeafd16e2ec370f921c9`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7459d1296321411777affabf80d090b1fbecc4657eb59595843358339c6312b0`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 15.3 MB (15285512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed7d7067ab8c670931ca8b1189bd9a38826a73bd85738bc7d39984c644130c`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e4d0b6d559dc7e5813daa5608628d05948befcd4a15376cefb2e367a207e28`  
		Last Modified: Tue, 13 Aug 2024 01:20:29 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73efc838234869d78cc026e990490f94bac9917ef8173cbaa5e779339909fc3b`  
		Last Modified: Tue, 13 Aug 2024 01:20:31 GMT  
		Size: 134.5 MB (134454538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20c1e095b0f267f035dc7e31426a088d74274bd66f91e8111f23ae3df2c7f66`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b38537e038091ed75237387ec86924b0038c6ca335ab6f3e2adfb5275e541c2`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4ec1205180dcf1b27f844ac2b1928ec5a6ce3d38b770e65811b8f53fa3857`  
		Last Modified: Tue, 13 Aug 2024 01:20:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:768063bfdab5099b0fa869f9948135fc4ef46f2460cd231d8c169df32c93203b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e48e9480f68405cadd927fcac632f93919f262e97f4de0c984b2c23004655f4`

```dockerfile
```

-	Layers:
	-	`sha256:35ce39bc321eec5395ba1ee5f11c00221baf5503c2a0d93a22940fe6d1cc47cc`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57d962fde7e57bfa50c345f120cf2f1820877b7334b3bc8e17274aa6f2fe8b31`  
		Last Modified: Tue, 13 Aug 2024 01:20:28 GMT  
		Size: 34.1 KB (34137 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-oracle`

```console
$ docker pull mysql@sha256:c253b12ccf0c8b291af74f49cb7871bd822a0c71fb6d53d2e1c9f21b5f09b2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.39-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:0cb3ab06963a548f8eebb5aca9e06a0ea86db8178030f2e12edda36143a41259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167066842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8c3640577ec4c7a337d2376517832100a8df15b898e1cd4556750029804ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501b7dd297efa7df14b181f530712c03e4d07d7392768487270bd4402d4973`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c3c8425aebc06e1bb837ed9c09de67f979e209801f9797172b43c7ac1c374`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e545ccd1cfca01bba9cf729e86d46d7ff2656bc1ed3f94e24cc4fc4ce1613eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.7 MB (6731692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd749ad2b919b92916e0a41d9b266612ccb4ea70c6eaa71d4580b430b5c6a`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85a79daec728d49fdd898382156dc08eb4dadc0be7d9b7191842d9c34d037`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbbbba665339ec8f25cc36dc3158c64b2e11414f723532aff207c9777a78ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 49.2 MB (49178891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1253e3c023cd06fe203f4604165d2359a8d17694f02920ba62f09befbbb6419`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bd751a6d962970ee08cc2419b9a8a5207794cd6dc9584fe7b4f885dcc02a2`  
		Last Modified: Fri, 23 Aug 2024 01:50:59 GMT  
		Size: 60.9 MB (60929605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73384984c3a6f1f6027b09e0be131a98fd3a582b8d64944006d52d2fc33ab5`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e706c318d8c0d30be02562309b3ca1449c94cb7c9bdb6049e0f0e859bad7c3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fdfb587eefe3f939448c40150bd3ca1eacef355be061a97538396da8e1fa5e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13839976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2672e5e37229751c02f34512e9f981a0f5173414e023e1bdf812bfd0027424`

```dockerfile
```

-	Layers:
	-	`sha256:74f136e8de607d9fee65502f44e2769110992dfa06033910c0e6c82000c9172f`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.8 MB (13805195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486712bc68c230afa0305cf4b01c18470d0136ecd5c96910b16d2b81f8a1acaa`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.39-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:05343927ef5abe24dc77fa24e42719d1be3aa5c6f18d839cd5733126a581a993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0097b8a9d94b29005a790aba94aff0b3de55ef46e868ba3dc6975c516392d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6119f7988c09f46c88dabc21de5ee71f3037389bf54f65745c144c8981f70`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ffc2a6281d83ada9945b1c2c3ee58e84e40488c95ea612ad24b685c0ef3c3`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 48.1 MB (48056781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20aaad5eace96cf23c69b9bc5216570e66e36e7802208dc836ea51409493344`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f116c04068ffa62559cc40b1164c4443f8a45302338379c3ade4c8a43053ccd`  
		Last Modified: Fri, 23 Aug 2024 01:53:37 GMT  
		Size: 68.4 MB (68421591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdec858f245296d1c7329e536ea978fb1ef04c1683bd433cdd88809bf628b59`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d18518856de073ebf464e4e2698e2a5f2ff4ed863d8ba3283507a61d86ed9`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:38edee0b4107ea4224a6abc79f7b953591b3e5186057fcdc9fb859299ff6244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13835385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4022476141f42ba29d81e8b51fc6177e2b47b33e42636d66ccd321742391f`

```dockerfile
```

-	Layers:
	-	`sha256:026ac9441b137f1469427e14e8ff66b9433da6760407da5a03fa0df832f23044`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 13.8 MB (13800273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f9611fc5d846f7663a5a8e266db59eac25a036223a28ef04f4d500c1f066e`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-oraclelinux9`

```console
$ docker pull mysql@sha256:c253b12ccf0c8b291af74f49cb7871bd822a0c71fb6d53d2e1c9f21b5f09b2a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.39-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:0cb3ab06963a548f8eebb5aca9e06a0ea86db8178030f2e12edda36143a41259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167066842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd8c3640577ec4c7a337d2376517832100a8df15b898e1cd4556750029804ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7501b7dd297efa7df14b181f530712c03e4d07d7392768487270bd4402d4973`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398c3c8425aebc06e1bb837ed9c09de67f979e209801f9797172b43c7ac1c374`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e545ccd1cfca01bba9cf729e86d46d7ff2656bc1ed3f94e24cc4fc4ce1613eb`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.7 MB (6731692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccd749ad2b919b92916e0a41d9b266612ccb4ea70c6eaa71d4580b430b5c6a`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea85a79daec728d49fdd898382156dc08eb4dadc0be7d9b7191842d9c34d037`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ecbbbba665339ec8f25cc36dc3158c64b2e11414f723532aff207c9777a78ba`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 49.2 MB (49178891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1253e3c023cd06fe203f4604165d2359a8d17694f02920ba62f09befbbb6419`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:764bd751a6d962970ee08cc2419b9a8a5207794cd6dc9584fe7b4f885dcc02a2`  
		Last Modified: Fri, 23 Aug 2024 01:50:59 GMT  
		Size: 60.9 MB (60929605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d73384984c3a6f1f6027b09e0be131a98fd3a582b8d64944006d52d2fc33ab5`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e706c318d8c0d30be02562309b3ca1449c94cb7c9bdb6049e0f0e859bad7c3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fdfb587eefe3f939448c40150bd3ca1eacef355be061a97538396da8e1fa5e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13839976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2672e5e37229751c02f34512e9f981a0f5173414e023e1bdf812bfd0027424`

```dockerfile
```

-	Layers:
	-	`sha256:74f136e8de607d9fee65502f44e2769110992dfa06033910c0e6c82000c9172f`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.8 MB (13805195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:486712bc68c230afa0305cf4b01c18470d0136ecd5c96910b16d2b81f8a1acaa`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.39-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:05343927ef5abe24dc77fa24e42719d1be3aa5c6f18d839cd5733126a581a993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.6 MB (171621163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0097b8a9d94b29005a790aba94aff0b3de55ef46e868ba3dc6975c516392d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_VERSION=8.0.39-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Mon, 22 Jul 2024 22:26:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:26:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 22 Jul 2024 22:26:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:26:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:26:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b6119f7988c09f46c88dabc21de5ee71f3037389bf54f65745c144c8981f70`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2ffc2a6281d83ada9945b1c2c3ee58e84e40488c95ea612ad24b685c0ef3c3`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 48.1 MB (48056781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20aaad5eace96cf23c69b9bc5216570e66e36e7802208dc836ea51409493344`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f116c04068ffa62559cc40b1164c4443f8a45302338379c3ade4c8a43053ccd`  
		Last Modified: Fri, 23 Aug 2024 01:53:37 GMT  
		Size: 68.4 MB (68421591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdec858f245296d1c7329e536ea978fb1ef04c1683bd433cdd88809bf628b59`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0d18518856de073ebf464e4e2698e2a5f2ff4ed863d8ba3283507a61d86ed9`  
		Last Modified: Fri, 23 Aug 2024 01:53:36 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:38edee0b4107ea4224a6abc79f7b953591b3e5186057fcdc9fb859299ff6244f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13835385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd4022476141f42ba29d81e8b51fc6177e2b47b33e42636d66ccd321742391f`

```dockerfile
```

-	Layers:
	-	`sha256:026ac9441b137f1469427e14e8ff66b9433da6760407da5a03fa0df832f23044`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 13.8 MB (13800273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:285f9611fc5d846f7663a5a8e266db59eac25a036223a28ef04f4d500c1f066e`  
		Last Modified: Fri, 23 Aug 2024 01:53:35 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.2` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2-oracle`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2-oraclelinux9`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oracle`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oraclelinux9`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.1` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1-oracle`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1-oraclelinux9`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:ad77a7c4e2031597e0c73a21993f780cdde6cef15d3dae734fe550c6142f8097
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:12f800accdf4aacff75dc1b00a41b17be628240e9f6f8cb355a185df4f86e151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.8 MB (169760878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:750b67184e7aeeb9d1bf9279cd311502a17a2d9fa230c77b332d3b51655209f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6ddf56df3246c729cbb5e4c241200d3528a5e2602251da2d3cede6dff77b4b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ea8d4b0b4c11061fc3461c2e1a44fc21ce31b76bfaca5ffdd529d5006663b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 6.7 MB (6731657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7831e46745cb33979acba0e1e4f928cc8c6cc11bec6db7fd1eec50a904f3730`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68dfd038d6fe612b7e5a1bf5566078d5ea49f4a4c761623191b8fdc726afd8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:400f83c08f6007abcb5824a4b2d6ac45ddabb9036fa722a84637076028625863`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.3 MB (47251371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f688763fd15221f021296119966923d4caf860270bcf267191bdafe0002302a3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c44c25a80a1a42cb0f5c383adc7e3ef9536f600d90f31bf4155d42d67deea43`  
		Last Modified: Fri, 23 Aug 2024 01:50:57 GMT  
		Size: 65.6 MB (65551315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2d80756f3dd4d62b9b6eb4f5b5f79875f0cdebaada60d7e192dea098383eea`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9119bbe565c193c2f5f0a37803a29f1bb39efd5002d34c740bfe0e9f2e5dce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:000e2372b8196db15e17cf6dfb14e0b09a2495bf6e92ee37b1854a41e07a2723`

```dockerfile
```

-	Layers:
	-	`sha256:4bfc1e7b8f9f786ce339aac62e168e69c772910d814f88f04d28ff52447275e4`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 13.9 MB (13915212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:446537175f3f5c797d2d3e25759f857e7bd60491bae80bd23d9cae1ca8ce5537`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:19b3ba2b959ec564bc25d09b2a04a2cb1558be581ba3d0b31d7515d6727efdb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167044178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a5e588a69b61a4bceecc29979e2b1eea4e096eb3a108a9d9a842959fcead84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_VERSION=8.4.2-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Mon, 22 Jul 2024 22:32:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:32:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:32:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:32:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235f6a16f5433dff0dc333a4dfaf9bee514cf9f2b4643e7c7a5c8a31de66671f`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6aaf631f1da935067f9b33be1de24877112925d1dd0b620940d128ca33d1f8`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 46.1 MB (46147843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b83eb9ad50da25416f30c7d72356fe24194254b789b96471941242dad46d52`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b971475b2b087a4e3d7254f7bdffd9ada8b323b4fc314a7518f45d9fde6cb84`  
		Last Modified: Fri, 23 Aug 2024 01:52:17 GMT  
		Size: 65.8 MB (65753663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa369cdb9f9d2a3222cea7c086fe7730f88714bef9e3f3d2f12b6c99b170856`  
		Last Modified: Fri, 23 Aug 2024 01:52:16 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7557e146df06089e393affb7c2a79cc4d50d551521238535e645d2ccf57069a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13944837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10707bd4698bc855797a2706ce8c037b6f11b78b5eafa1adc2d30e3155b16782`

```dockerfile
```

-	Layers:
	-	`sha256:e16b0f2e3137a63b54e813e0aa1f4db7b57a2d4fdda8f5f9cefe6382d6df92b1`  
		Last Modified: Fri, 23 Aug 2024 01:52:15 GMT  
		Size: 13.9 MB (13910362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2520c71cf3bdaf09c6e0003440fa394c643c5f2940c00e797889dde1a332f1af`  
		Last Modified: Fri, 23 Aug 2024 01:52:14 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:86cdfe832c81e39a89cfb63c3fde1683c41cc00ef91e67653c9c1df0ba80f454
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e5ab70d6583fab7597870a1c3599059be44648649d59b0e75e50726ab4c42bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170562604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82a8f162e188e0df15b0d2d90c6e9e973af8e88a6cb74b8052122ae5e02325c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:8c9ab8771c54dd850765999ece3b2f78bf01722be026d3a4da07f0c726c196b3 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6e839ac3722d35bc5d6a0df7fb05dec1ec11afffad55cbfe7d3ab862d86ae0ac`  
		Last Modified: Fri, 23 Aug 2024 01:21:56 GMT  
		Size: 49.2 MB (49234064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad912193ad5fb26a0276f1f74835d9ca84a174817d522b42188b495df5715d8a`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d13d87fd8da097505c3c6a52573e46eff6c24bec624047ab5a9f3a7602e92c`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 983.0 KB (983002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:004d383c75ef8fe45e104dc1877dc45e1f079fbb0a62ab7e657a50ad69db7f64`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 6.7 MB (6731636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbc82a0b8ccb2827ab30b19fd7a323d70062a683e8161af2ac9df9bea7835`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fec07ea5501fdb66d2bca2d60605f53c56e43805f2c4139405e256d6de94b7`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83357cb2d3a578a53aae75b12f0ca7648647f1ca17b539ded415b3613e103276`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 47.7 MB (47707474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ffe968b82c12164dcf09758d749d68c96a9d35e013d14be3f77003ff9b25b17`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30dfd9a7ed5737f0f7afa2f8a5d6d0baa862273ac005269857acd294cd3fd0b0`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 65.9 MB (65896944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35844ae33cbebd575baf9ca73fafe993c44bce10e351ee0cf977f7667c44967d`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6a8123668fbe451a51f562383dd98187ed9327e69f18b9760cc7cf41e0408940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.0 MB (13953969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0208bc0c076e65c50e86655c4fec46ad338206701e18412f68548a1896bcc624`

```dockerfile
```

-	Layers:
	-	`sha256:052ac79809a02bed6f7d8c54d766b9b7264f768bfadfe744479cbc8e4c68da3d`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13918829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddec6842ec678be48adc870a48940b8c43384328438f251c5d15c636bf43a7ad`  
		Last Modified: Fri, 23 Aug 2024 01:50:53 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a6e00e4043c02e67565eeb1cae1ada064adea1bcaf7c329ec960087c4fc8777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167826186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f958d2869db0ad05333c6eb75ddd94a397846e65e841dc37c93120837ba3c769`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:f2c8ba57b2cbd322d81b3c1d19d7f39b04f3cee01184d71bbb4e03f5dc6f9023 in / 
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["/bin/bash"]
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV GOSU_VERSION=1.17
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENV MYSQL_SHELL_VERSION=9.0.1-1.el9
# Mon, 22 Jul 2024 22:36:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
VOLUME [/var/lib/mysql]
# Mon, 22 Jul 2024 22:36:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Jul 2024 22:36:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 22 Jul 2024 22:36:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 22 Jul 2024 22:36:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:86a1ed2ecedfb25be946a0e5d6d7461438be946bd1a1ef41216e731ca9d42959`  
		Last Modified: Fri, 23 Aug 2024 00:41:39 GMT  
		Size: 47.9 MB (47887791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf88b6547cb54d62e93b41fcb1d3c9d2f2ffeccaf130182c824ed07a8324e93b`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b5914950d67c45f302a837ed7c093e2d3f676a37465f1b9ce6b981c1186e9`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c617af9dc74d8a336a3c01a28b7c279a2570876c90803cbf311af54a2a4f1570`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 6.3 MB (6331972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e52819b0ae225da19408bf66a924da16a415a969d73e58110b737824b7e7664`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5287643f1002b5a64680de318210ec98de79039ac4cc851de0cc715e365643e7`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f4c36d9f513714ce1424a2a60a76cb09b42f94b2455577e621e0f7f3a67b3c`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 46.6 MB (46606057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6961d55922757b9f52264e44757e9e490dc23cc79a0770353f19b55c42826b`  
		Last Modified: Fri, 23 Aug 2024 01:50:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de886bf754cb7c9cdd41476c690515e4bb656d2c36f2e4a64fc5e39c5bfc903a`  
		Last Modified: Fri, 23 Aug 2024 01:50:58 GMT  
		Size: 66.1 MB (66077448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d62dc59968bd4ea4fd378ed69d04f1de0644251cd9bbd9639ed0f880c7827e3`  
		Last Modified: Fri, 23 Aug 2024 01:50:56 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2a0571db2c8f5e4ca8118d053f6080b34811ecffb2ca905f3fa6317f81202547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13949594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5af93abf9586e9cd4c2646e91fc42d2d1f89ebcaa119a77d4c386aa836a0262`

```dockerfile
```

-	Layers:
	-	`sha256:6762ce1b758b919d07757b34fe3a670eba0b707ee69aae1e12a8e4fa16517129`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 13.9 MB (13914015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bc849ec71f8487886067d58282ee4c401581ce1523f54ffc6c5143d17dbd004`  
		Last Modified: Fri, 23 Aug 2024 01:50:54 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
