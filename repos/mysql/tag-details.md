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
-	[`mysql:8.0.44`](#mysql8044)
-	[`mysql:8.0.44-bookworm`](#mysql8044-bookworm)
-	[`mysql:8.0.44-debian`](#mysql8044-debian)
-	[`mysql:8.0.44-oracle`](#mysql8044-oracle)
-	[`mysql:8.0.44-oraclelinux9`](#mysql8044-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.7`](#mysql847)
-	[`mysql:8.4.7-oracle`](#mysql847-oracle)
-	[`mysql:8.4.7-oraclelinux9`](#mysql847-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.5`](#mysql95)
-	[`mysql:9.5-oracle`](#mysql95-oracle)
-	[`mysql:9.5-oraclelinux9`](#mysql95-oraclelinux9)
-	[`mysql:9.5.0`](#mysql950)
-	[`mysql:9.5.0-oracle`](#mysql950-oracle)
-	[`mysql:9.5.0-oraclelinux9`](#mysql950-oraclelinux9)
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
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:c7d30101340e026247603b13dba80bf8075b4378aee39d1989a2a63c4e929c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:df53894b07c97c531592ea1e44b04e5efcd416f0250c308051fbc5d19bcda6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232077346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5c3ce040b7f2cf5e29c1d13f1fac8cf289f80a4e5923176288ba0309185cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:56:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71d99754e7fce47a96b019d5b015fa82b14654e2b317def988640790577816`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afab7cd73c9a0d356d76775b76f60ca97443bb66d9ae48d85b315d4de5256`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a23e1c40841aebf95515a25dbe361f152b5cd3a5d3d48250bcae77cd0ce617`  
		Last Modified: Mon, 01 Dec 2025 23:57:17 GMT  
		Size: 6.2 MB (6171680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba22cf5fa74c55db52e964b0ac26487b83029fba1a728245ecc5ca10faf18`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3ee3949612a64c5485b87e88c4986b3dca9ac63d12c711fdb238d285755b5`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482b81b924f28a4b5c55eb155d3ffe5bc12ef16c3ea8af96a373254f84f114`  
		Last Modified: Mon, 01 Dec 2025 23:57:24 GMT  
		Size: 49.9 MB (49912466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8a054444545f3860b800e5d4772c600c78a935c5e9cbe2f6c74187881f88`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ca50ef0af7e47a3ce9d62ecbf2284c44cd88e0c00f4b1e5bc109361c529c`  
		Last Modified: Mon, 01 Dec 2025 23:57:25 GMT  
		Size: 127.9 MB (127887874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e015324be13d859e1cb9cc057b4ffdf343afeac69aa1b94e8aecd2967eb91`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5065de1ac5292fd648699c663a1d87bde156d4bc6e5321728bec8031aec4552`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1b4143ad6f1901c7928d3fde7c4544e9ab1a0e0f4e675b375d014d90da516a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339ad01127b6e0b5d1201c19f15a4dd5696be9fbb595684284df9369173f57f9`

```dockerfile
```

-	Layers:
	-	`sha256:8b4682407a3b66ba9dd055d3a964230936f4a97ea4f8a2ba307a3d5bfae9ea91`  
		Last Modified: Tue, 02 Dec 2025 01:02:46 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf8e6c8ffc3f81d41b1810a65f0bdcda119d4d3b47c08b5275518b5f3a8ab6`  
		Last Modified: Tue, 02 Dec 2025 01:02:47 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6718e067dcd66e049fe76221f79f6dc162e5f07371d9ce0ede793b6b9cddfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e432af9da0e8f839a5ade9cf5d1508a8f78d2ef67b037fb48af4744f8f8e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:01:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceed42538b5cec16115540ee4d52f450703f480aba57712c3e36393668312a`  
		Last Modified: Tue, 02 Dec 2025 00:02:24 GMT  
		Size: 5.8 MB (5796066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbddb48ebfb623f99e9a9a861729996cb6bba74a9de47bacb5382d51c446ba7`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb88b0a00f535736dfd9ba29854f3ff7059295f62e8ac72c9808d63d8898e01`  
		Last Modified: Tue, 02 Dec 2025 00:02:21 GMT  
		Size: 48.8 MB (48782364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb47184d91a97541bce7c7809aff110361a01b4182343ae2ddf6dd7b3a5974`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0ad4e8ef4afe2fbbb196a72370b7db336103d55b6a28ccb046df85976aa7a`  
		Last Modified: Tue, 02 Dec 2025 00:02:27 GMT  
		Size: 126.5 MB (126468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606a3120e763400c5163f50ba28aeb90c5d68aafd80a63fd293a828b3f3c49d`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf1de95b62bdb43a81c7009e49b2b148c056224b1c51baee3ecce9ca19d494`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f71d365a9301a118e2a91f6cf98268202551987441fced070c61ab61947bccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106af921886481ded9c5a1a7347e94071e36f0ab14220aae8fd434565def4bc`

```dockerfile
```

-	Layers:
	-	`sha256:079fdfeb7777aa514bf2873bcb970e7c5c3a80e6aa7e804dd02ada0f6c6655e4`  
		Last Modified: Tue, 02 Dec 2025 01:02:56 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3a00d4c16afb4e68b160db7d5ca067ab70dbe3333029b93b05c52c31fdd2f8`  
		Last Modified: Tue, 02 Dec 2025 01:02:57 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:c7d30101340e026247603b13dba80bf8075b4378aee39d1989a2a63c4e929c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df53894b07c97c531592ea1e44b04e5efcd416f0250c308051fbc5d19bcda6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232077346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5c3ce040b7f2cf5e29c1d13f1fac8cf289f80a4e5923176288ba0309185cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:56:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71d99754e7fce47a96b019d5b015fa82b14654e2b317def988640790577816`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afab7cd73c9a0d356d76775b76f60ca97443bb66d9ae48d85b315d4de5256`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a23e1c40841aebf95515a25dbe361f152b5cd3a5d3d48250bcae77cd0ce617`  
		Last Modified: Mon, 01 Dec 2025 23:57:17 GMT  
		Size: 6.2 MB (6171680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba22cf5fa74c55db52e964b0ac26487b83029fba1a728245ecc5ca10faf18`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3ee3949612a64c5485b87e88c4986b3dca9ac63d12c711fdb238d285755b5`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482b81b924f28a4b5c55eb155d3ffe5bc12ef16c3ea8af96a373254f84f114`  
		Last Modified: Mon, 01 Dec 2025 23:57:24 GMT  
		Size: 49.9 MB (49912466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8a054444545f3860b800e5d4772c600c78a935c5e9cbe2f6c74187881f88`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ca50ef0af7e47a3ce9d62ecbf2284c44cd88e0c00f4b1e5bc109361c529c`  
		Last Modified: Mon, 01 Dec 2025 23:57:25 GMT  
		Size: 127.9 MB (127887874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e015324be13d859e1cb9cc057b4ffdf343afeac69aa1b94e8aecd2967eb91`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5065de1ac5292fd648699c663a1d87bde156d4bc6e5321728bec8031aec4552`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1b4143ad6f1901c7928d3fde7c4544e9ab1a0e0f4e675b375d014d90da516a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339ad01127b6e0b5d1201c19f15a4dd5696be9fbb595684284df9369173f57f9`

```dockerfile
```

-	Layers:
	-	`sha256:8b4682407a3b66ba9dd055d3a964230936f4a97ea4f8a2ba307a3d5bfae9ea91`  
		Last Modified: Tue, 02 Dec 2025 01:02:46 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf8e6c8ffc3f81d41b1810a65f0bdcda119d4d3b47c08b5275518b5f3a8ab6`  
		Last Modified: Tue, 02 Dec 2025 01:02:47 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6718e067dcd66e049fe76221f79f6dc162e5f07371d9ce0ede793b6b9cddfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e432af9da0e8f839a5ade9cf5d1508a8f78d2ef67b037fb48af4744f8f8e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:01:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceed42538b5cec16115540ee4d52f450703f480aba57712c3e36393668312a`  
		Last Modified: Tue, 02 Dec 2025 00:02:24 GMT  
		Size: 5.8 MB (5796066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbddb48ebfb623f99e9a9a861729996cb6bba74a9de47bacb5382d51c446ba7`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb88b0a00f535736dfd9ba29854f3ff7059295f62e8ac72c9808d63d8898e01`  
		Last Modified: Tue, 02 Dec 2025 00:02:21 GMT  
		Size: 48.8 MB (48782364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb47184d91a97541bce7c7809aff110361a01b4182343ae2ddf6dd7b3a5974`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0ad4e8ef4afe2fbbb196a72370b7db336103d55b6a28ccb046df85976aa7a`  
		Last Modified: Tue, 02 Dec 2025 00:02:27 GMT  
		Size: 126.5 MB (126468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606a3120e763400c5163f50ba28aeb90c5d68aafd80a63fd293a828b3f3c49d`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf1de95b62bdb43a81c7009e49b2b148c056224b1c51baee3ecce9ca19d494`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f71d365a9301a118e2a91f6cf98268202551987441fced070c61ab61947bccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106af921886481ded9c5a1a7347e94071e36f0ab14220aae8fd434565def4bc`

```dockerfile
```

-	Layers:
	-	`sha256:079fdfeb7777aa514bf2873bcb970e7c5c3a80e6aa7e804dd02ada0f6c6655e4`  
		Last Modified: Tue, 02 Dec 2025 01:02:56 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3a00d4c16afb4e68b160db7d5ca067ab70dbe3333029b93b05c52c31fdd2f8`  
		Last Modified: Tue, 02 Dec 2025 01:02:57 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c7d30101340e026247603b13dba80bf8075b4378aee39d1989a2a63c4e929c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df53894b07c97c531592ea1e44b04e5efcd416f0250c308051fbc5d19bcda6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232077346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5c3ce040b7f2cf5e29c1d13f1fac8cf289f80a4e5923176288ba0309185cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:56:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71d99754e7fce47a96b019d5b015fa82b14654e2b317def988640790577816`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afab7cd73c9a0d356d76775b76f60ca97443bb66d9ae48d85b315d4de5256`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a23e1c40841aebf95515a25dbe361f152b5cd3a5d3d48250bcae77cd0ce617`  
		Last Modified: Mon, 01 Dec 2025 23:57:17 GMT  
		Size: 6.2 MB (6171680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba22cf5fa74c55db52e964b0ac26487b83029fba1a728245ecc5ca10faf18`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3ee3949612a64c5485b87e88c4986b3dca9ac63d12c711fdb238d285755b5`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482b81b924f28a4b5c55eb155d3ffe5bc12ef16c3ea8af96a373254f84f114`  
		Last Modified: Mon, 01 Dec 2025 23:57:24 GMT  
		Size: 49.9 MB (49912466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8a054444545f3860b800e5d4772c600c78a935c5e9cbe2f6c74187881f88`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ca50ef0af7e47a3ce9d62ecbf2284c44cd88e0c00f4b1e5bc109361c529c`  
		Last Modified: Mon, 01 Dec 2025 23:57:25 GMT  
		Size: 127.9 MB (127887874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e015324be13d859e1cb9cc057b4ffdf343afeac69aa1b94e8aecd2967eb91`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5065de1ac5292fd648699c663a1d87bde156d4bc6e5321728bec8031aec4552`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1b4143ad6f1901c7928d3fde7c4544e9ab1a0e0f4e675b375d014d90da516a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339ad01127b6e0b5d1201c19f15a4dd5696be9fbb595684284df9369173f57f9`

```dockerfile
```

-	Layers:
	-	`sha256:8b4682407a3b66ba9dd055d3a964230936f4a97ea4f8a2ba307a3d5bfae9ea91`  
		Last Modified: Tue, 02 Dec 2025 01:02:46 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf8e6c8ffc3f81d41b1810a65f0bdcda119d4d3b47c08b5275518b5f3a8ab6`  
		Last Modified: Tue, 02 Dec 2025 01:02:47 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6718e067dcd66e049fe76221f79f6dc162e5f07371d9ce0ede793b6b9cddfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e432af9da0e8f839a5ade9cf5d1508a8f78d2ef67b037fb48af4744f8f8e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:01:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceed42538b5cec16115540ee4d52f450703f480aba57712c3e36393668312a`  
		Last Modified: Tue, 02 Dec 2025 00:02:24 GMT  
		Size: 5.8 MB (5796066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbddb48ebfb623f99e9a9a861729996cb6bba74a9de47bacb5382d51c446ba7`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb88b0a00f535736dfd9ba29854f3ff7059295f62e8ac72c9808d63d8898e01`  
		Last Modified: Tue, 02 Dec 2025 00:02:21 GMT  
		Size: 48.8 MB (48782364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb47184d91a97541bce7c7809aff110361a01b4182343ae2ddf6dd7b3a5974`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0ad4e8ef4afe2fbbb196a72370b7db336103d55b6a28ccb046df85976aa7a`  
		Last Modified: Tue, 02 Dec 2025 00:02:27 GMT  
		Size: 126.5 MB (126468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606a3120e763400c5163f50ba28aeb90c5d68aafd80a63fd293a828b3f3c49d`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf1de95b62bdb43a81c7009e49b2b148c056224b1c51baee3ecce9ca19d494`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f71d365a9301a118e2a91f6cf98268202551987441fced070c61ab61947bccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106af921886481ded9c5a1a7347e94071e36f0ab14220aae8fd434565def4bc`

```dockerfile
```

-	Layers:
	-	`sha256:079fdfeb7777aa514bf2873bcb970e7c5c3a80e6aa7e804dd02ada0f6c6655e4`  
		Last Modified: Tue, 02 Dec 2025 01:02:56 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3a00d4c16afb4e68b160db7d5ca067ab70dbe3333029b93b05c52c31fdd2f8`  
		Last Modified: Tue, 02 Dec 2025 01:02:57 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44`

```console
$ docker pull mysql@sha256:c7d30101340e026247603b13dba80bf8075b4378aee39d1989a2a63c4e929c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44` - linux; amd64

```console
$ docker pull mysql@sha256:df53894b07c97c531592ea1e44b04e5efcd416f0250c308051fbc5d19bcda6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232077346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5c3ce040b7f2cf5e29c1d13f1fac8cf289f80a4e5923176288ba0309185cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:56:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71d99754e7fce47a96b019d5b015fa82b14654e2b317def988640790577816`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afab7cd73c9a0d356d76775b76f60ca97443bb66d9ae48d85b315d4de5256`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a23e1c40841aebf95515a25dbe361f152b5cd3a5d3d48250bcae77cd0ce617`  
		Last Modified: Mon, 01 Dec 2025 23:57:17 GMT  
		Size: 6.2 MB (6171680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba22cf5fa74c55db52e964b0ac26487b83029fba1a728245ecc5ca10faf18`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3ee3949612a64c5485b87e88c4986b3dca9ac63d12c711fdb238d285755b5`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482b81b924f28a4b5c55eb155d3ffe5bc12ef16c3ea8af96a373254f84f114`  
		Last Modified: Mon, 01 Dec 2025 23:57:24 GMT  
		Size: 49.9 MB (49912466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8a054444545f3860b800e5d4772c600c78a935c5e9cbe2f6c74187881f88`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ca50ef0af7e47a3ce9d62ecbf2284c44cd88e0c00f4b1e5bc109361c529c`  
		Last Modified: Mon, 01 Dec 2025 23:57:25 GMT  
		Size: 127.9 MB (127887874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e015324be13d859e1cb9cc057b4ffdf343afeac69aa1b94e8aecd2967eb91`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5065de1ac5292fd648699c663a1d87bde156d4bc6e5321728bec8031aec4552`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:1b4143ad6f1901c7928d3fde7c4544e9ab1a0e0f4e675b375d014d90da516a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339ad01127b6e0b5d1201c19f15a4dd5696be9fbb595684284df9369173f57f9`

```dockerfile
```

-	Layers:
	-	`sha256:8b4682407a3b66ba9dd055d3a964230936f4a97ea4f8a2ba307a3d5bfae9ea91`  
		Last Modified: Tue, 02 Dec 2025 01:02:46 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf8e6c8ffc3f81d41b1810a65f0bdcda119d4d3b47c08b5275518b5f3a8ab6`  
		Last Modified: Tue, 02 Dec 2025 01:02:47 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6718e067dcd66e049fe76221f79f6dc162e5f07371d9ce0ede793b6b9cddfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e432af9da0e8f839a5ade9cf5d1508a8f78d2ef67b037fb48af4744f8f8e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:01:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceed42538b5cec16115540ee4d52f450703f480aba57712c3e36393668312a`  
		Last Modified: Tue, 02 Dec 2025 00:02:24 GMT  
		Size: 5.8 MB (5796066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbddb48ebfb623f99e9a9a861729996cb6bba74a9de47bacb5382d51c446ba7`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb88b0a00f535736dfd9ba29854f3ff7059295f62e8ac72c9808d63d8898e01`  
		Last Modified: Tue, 02 Dec 2025 00:02:21 GMT  
		Size: 48.8 MB (48782364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb47184d91a97541bce7c7809aff110361a01b4182343ae2ddf6dd7b3a5974`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0ad4e8ef4afe2fbbb196a72370b7db336103d55b6a28ccb046df85976aa7a`  
		Last Modified: Tue, 02 Dec 2025 00:02:27 GMT  
		Size: 126.5 MB (126468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606a3120e763400c5163f50ba28aeb90c5d68aafd80a63fd293a828b3f3c49d`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf1de95b62bdb43a81c7009e49b2b148c056224b1c51baee3ecce9ca19d494`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44` - unknown; unknown

```console
$ docker pull mysql@sha256:f71d365a9301a118e2a91f6cf98268202551987441fced070c61ab61947bccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106af921886481ded9c5a1a7347e94071e36f0ab14220aae8fd434565def4bc`

```dockerfile
```

-	Layers:
	-	`sha256:079fdfeb7777aa514bf2873bcb970e7c5c3a80e6aa7e804dd02ada0f6c6655e4`  
		Last Modified: Tue, 02 Dec 2025 01:02:56 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3a00d4c16afb4e68b160db7d5ca067ab70dbe3333029b93b05c52c31fdd2f8`  
		Last Modified: Tue, 02 Dec 2025 01:02:57 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-bookworm`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-debian`

```console
$ docker pull mysql@sha256:9a83525860305d8add9138b85c17a9bf0df110f519a530d1045dcd42c7990738
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.44-debian` - linux; amd64

```console
$ docker pull mysql@sha256:4870362fd35c2b417ea03abb4b488131fc092bfdf29e9190a118e42f46564cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183456846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f2500c5804ed4c389bd94081768c68cb6daecdecca35b7dd9099fecdbd7e39e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Tue, 18 Nov 2025 05:18:18 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Nov 2025 05:18:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
ENV GOSU_VERSION=1.19
# Tue, 18 Nov 2025 05:18:29 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Nov 2025 05:18:29 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Nov 2025 05:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Nov 2025 05:18:34 GMT
ENV MYSQL_VERSION=8.0.44-1debian12
# Tue, 18 Nov 2025 05:18:34 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Nov 2025 05:18:44 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Nov 2025 05:18:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Nov 2025 05:18:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Nov 2025 05:18:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bc1ee5df0f5ddaa06ea6f137c5aaf84e6151e507d774b83a1e7e5927580497`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.1 KB (1104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fdcf29ca1901948dff2372cf804399684addcd394e41bdea15e44c082d056a0`  
		Last Modified: Tue, 18 Nov 2025 05:19:20 GMT  
		Size: 4.4 MB (4422994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718cf99aa376e1d1c7111c5e5d0d30ac43032e5a8ca5c7041d8f2d7eb0cae0e`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 1.2 MB (1248641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52c08b52775546d25b88d52e4a8797e54fd26ba4483c0e51e6148617aff5ba5`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2ff32950ede470fbf693afad9d266ba065b5642cad049b806896c2afd75f0b`  
		Last Modified: Tue, 18 Nov 2025 05:19:21 GMT  
		Size: 15.3 MB (15294574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd3ccf374c61a824dcf7d05f62fc65c1f723e2be1df32e7a811aa94628ef5683`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 3.1 KB (3052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506b564438516d55a59164c20dc0a70a6bd91d2a15be1c10a1bd54bcaaac87a3`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8bb26e367ce52f0171525fd52e97bfe5333b9063d932c9b23ccd1a075a88`  
		Last Modified: Tue, 18 Nov 2025 07:03:55 GMT  
		Size: 134.3 MB (134251368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5587f7d01add3e6098ab6843e841f176cefaf314cb6785f03bee3dee1ef048a`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f9aac72cfbcde02efeb3aef3fca37455cc9b2b52d132fd34c26b4c311705aa`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d28f7540fa18e43d086fbb5730e54cdac0ab3a2da64d54094d1f6f787f91359`  
		Last Modified: Tue, 18 Nov 2025 05:19:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ea8753eb61f3afcf8febe57f9f5f2c6b51a6cc95a485f4f3ca043337b58ac83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0383c231314495605d19b1ff84f66806b29f753fd699ef7af640ddfcbc4eb0cc`

```dockerfile
```

-	Layers:
	-	`sha256:b44d819af9229eb5ea4e04e0794d6a0b5a35c8e259df9e81d2c1c351b9e09469`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 4.2 MB (4163495 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd677d518ab7f245aa9c08a2482910f4c70e38082e6515493d5dce6d73cbfcd4`  
		Last Modified: Tue, 18 Nov 2025 07:03:14 GMT  
		Size: 34.3 KB (34252 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oracle`

```console
$ docker pull mysql@sha256:c7d30101340e026247603b13dba80bf8075b4378aee39d1989a2a63c4e929c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:df53894b07c97c531592ea1e44b04e5efcd416f0250c308051fbc5d19bcda6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232077346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5c3ce040b7f2cf5e29c1d13f1fac8cf289f80a4e5923176288ba0309185cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:56:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71d99754e7fce47a96b019d5b015fa82b14654e2b317def988640790577816`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afab7cd73c9a0d356d76775b76f60ca97443bb66d9ae48d85b315d4de5256`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a23e1c40841aebf95515a25dbe361f152b5cd3a5d3d48250bcae77cd0ce617`  
		Last Modified: Mon, 01 Dec 2025 23:57:17 GMT  
		Size: 6.2 MB (6171680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba22cf5fa74c55db52e964b0ac26487b83029fba1a728245ecc5ca10faf18`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3ee3949612a64c5485b87e88c4986b3dca9ac63d12c711fdb238d285755b5`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482b81b924f28a4b5c55eb155d3ffe5bc12ef16c3ea8af96a373254f84f114`  
		Last Modified: Mon, 01 Dec 2025 23:57:24 GMT  
		Size: 49.9 MB (49912466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8a054444545f3860b800e5d4772c600c78a935c5e9cbe2f6c74187881f88`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ca50ef0af7e47a3ce9d62ecbf2284c44cd88e0c00f4b1e5bc109361c529c`  
		Last Modified: Mon, 01 Dec 2025 23:57:25 GMT  
		Size: 127.9 MB (127887874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e015324be13d859e1cb9cc057b4ffdf343afeac69aa1b94e8aecd2967eb91`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5065de1ac5292fd648699c663a1d87bde156d4bc6e5321728bec8031aec4552`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1b4143ad6f1901c7928d3fde7c4544e9ab1a0e0f4e675b375d014d90da516a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339ad01127b6e0b5d1201c19f15a4dd5696be9fbb595684284df9369173f57f9`

```dockerfile
```

-	Layers:
	-	`sha256:8b4682407a3b66ba9dd055d3a964230936f4a97ea4f8a2ba307a3d5bfae9ea91`  
		Last Modified: Tue, 02 Dec 2025 01:02:46 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf8e6c8ffc3f81d41b1810a65f0bdcda119d4d3b47c08b5275518b5f3a8ab6`  
		Last Modified: Tue, 02 Dec 2025 01:02:47 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6718e067dcd66e049fe76221f79f6dc162e5f07371d9ce0ede793b6b9cddfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e432af9da0e8f839a5ade9cf5d1508a8f78d2ef67b037fb48af4744f8f8e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:01:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceed42538b5cec16115540ee4d52f450703f480aba57712c3e36393668312a`  
		Last Modified: Tue, 02 Dec 2025 00:02:24 GMT  
		Size: 5.8 MB (5796066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbddb48ebfb623f99e9a9a861729996cb6bba74a9de47bacb5382d51c446ba7`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb88b0a00f535736dfd9ba29854f3ff7059295f62e8ac72c9808d63d8898e01`  
		Last Modified: Tue, 02 Dec 2025 00:02:21 GMT  
		Size: 48.8 MB (48782364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb47184d91a97541bce7c7809aff110361a01b4182343ae2ddf6dd7b3a5974`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0ad4e8ef4afe2fbbb196a72370b7db336103d55b6a28ccb046df85976aa7a`  
		Last Modified: Tue, 02 Dec 2025 00:02:27 GMT  
		Size: 126.5 MB (126468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606a3120e763400c5163f50ba28aeb90c5d68aafd80a63fd293a828b3f3c49d`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf1de95b62bdb43a81c7009e49b2b148c056224b1c51baee3ecce9ca19d494`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f71d365a9301a118e2a91f6cf98268202551987441fced070c61ab61947bccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106af921886481ded9c5a1a7347e94071e36f0ab14220aae8fd434565def4bc`

```dockerfile
```

-	Layers:
	-	`sha256:079fdfeb7777aa514bf2873bcb970e7c5c3a80e6aa7e804dd02ada0f6c6655e4`  
		Last Modified: Tue, 02 Dec 2025 01:02:56 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3a00d4c16afb4e68b160db7d5ca067ab70dbe3333029b93b05c52c31fdd2f8`  
		Last Modified: Tue, 02 Dec 2025 01:02:57 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.44-oraclelinux9`

```console
$ docker pull mysql@sha256:c7d30101340e026247603b13dba80bf8075b4378aee39d1989a2a63c4e929c81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.44-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:df53894b07c97c531592ea1e44b04e5efcd416f0250c308051fbc5d19bcda6d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.1 MB (232077346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5c3ce040b7f2cf5e29c1d13f1fac8cf289f80a4e5923176288ba0309185cd7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:26 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:46 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 01 Dec 2025 23:55:47 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:55:47 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Mon, 01 Dec 2025 23:56:40 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 01 Dec 2025 23:56:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:40 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:40 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e71d99754e7fce47a96b019d5b015fa82b14654e2b317def988640790577816`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46afab7cd73c9a0d356d76775b76f60ca97443bb66d9ae48d85b315d4de5256`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a23e1c40841aebf95515a25dbe361f152b5cd3a5d3d48250bcae77cd0ce617`  
		Last Modified: Mon, 01 Dec 2025 23:57:17 GMT  
		Size: 6.2 MB (6171680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba22cf5fa74c55db52e964b0ac26487b83029fba1a728245ecc5ca10faf18`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3ee3949612a64c5485b87e88c4986b3dca9ac63d12c711fdb238d285755b5`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03482b81b924f28a4b5c55eb155d3ffe5bc12ef16c3ea8af96a373254f84f114`  
		Last Modified: Mon, 01 Dec 2025 23:57:24 GMT  
		Size: 49.9 MB (49912466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a8a054444545f3860b800e5d4772c600c78a935c5e9cbe2f6c74187881f88`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391ca50ef0af7e47a3ce9d62ecbf2284c44cd88e0c00f4b1e5bc109361c529c`  
		Last Modified: Mon, 01 Dec 2025 23:57:25 GMT  
		Size: 127.9 MB (127887874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9e015324be13d859e1cb9cc057b4ffdf343afeac69aa1b94e8aecd2967eb91`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5065de1ac5292fd648699c663a1d87bde156d4bc6e5321728bec8031aec4552`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1b4143ad6f1901c7928d3fde7c4544e9ab1a0e0f4e675b375d014d90da516a81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14655344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:339ad01127b6e0b5d1201c19f15a4dd5696be9fbb595684284df9369173f57f9`

```dockerfile
```

-	Layers:
	-	`sha256:8b4682407a3b66ba9dd055d3a964230936f4a97ea4f8a2ba307a3d5bfae9ea91`  
		Last Modified: Tue, 02 Dec 2025 01:02:46 GMT  
		Size: 14.6 MB (14620433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edaf8e6c8ffc3f81d41b1810a65f0bdcda119d4d3b47c08b5275518b5f3a8ab6`  
		Last Modified: Tue, 02 Dec 2025 01:02:47 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.44-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6718e067dcd66e049fe76221f79f6dc162e5f07371d9ce0ede793b6b9cddfe62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.7 MB (227690842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e432af9da0e8f839a5ade9cf5d1508a8f78d2ef67b037fb48af4744f8f8e745`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.0.44-1.el9
# Tue, 02 Dec 2025 00:01:31 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cceed42538b5cec16115540ee4d52f450703f480aba57712c3e36393668312a`  
		Last Modified: Tue, 02 Dec 2025 00:02:24 GMT  
		Size: 5.8 MB (5796066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbddb48ebfb623f99e9a9a861729996cb6bba74a9de47bacb5382d51c446ba7`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb88b0a00f535736dfd9ba29854f3ff7059295f62e8ac72c9808d63d8898e01`  
		Last Modified: Tue, 02 Dec 2025 00:02:21 GMT  
		Size: 48.8 MB (48782364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bb47184d91a97541bce7c7809aff110361a01b4182343ae2ddf6dd7b3a5974`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bb0ad4e8ef4afe2fbbb196a72370b7db336103d55b6a28ccb046df85976aa7a`  
		Last Modified: Tue, 02 Dec 2025 00:02:27 GMT  
		Size: 126.5 MB (126468313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3606a3120e763400c5163f50ba28aeb90c5d68aafd80a63fd293a828b3f3c49d`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ecf1de95b62bdb43a81c7009e49b2b148c056224b1c51baee3ecce9ca19d494`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.44-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f71d365a9301a118e2a91f6cf98268202551987441fced070c61ab61947bccf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.7 MB (14653940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106af921886481ded9c5a1a7347e94071e36f0ab14220aae8fd434565def4bc`

```dockerfile
```

-	Layers:
	-	`sha256:079fdfeb7777aa514bf2873bcb970e7c5c3a80e6aa7e804dd02ada0f6c6655e4`  
		Last Modified: Tue, 02 Dec 2025 01:02:56 GMT  
		Size: 14.6 MB (14618781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb3a00d4c16afb4e68b160db7d5ca067ab70dbe3333029b93b05c52c31fdd2f8`  
		Last Modified: Tue, 02 Dec 2025 01:02:57 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oracle`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.7-oraclelinux9`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.7-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.7-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.7-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oracle`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5-oraclelinux9`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oracle`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.5.0-oraclelinux9`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.5.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.5.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.5.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:ab61c921d5f5f6da7f62580a81b03eacbf0ad328850c4fa523850bcedad527f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f810f1d9bd07af336a798ece086525610e6c1206ff754e501bfe5665f342babb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233014126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cacc1f69b6b42e90d1173a4aee13aee907ca364683a1cef37135dc17da6f5c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:24 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:08 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Mon, 01 Dec 2025 23:56:38 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:38 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:38 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851012f95aee2ec8cbb32e9c8224db46821d6e5c7e09262211f873e689961336`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86eab596984c7865191fdd0ea9759e96e6d54ea83a1085c3773c08eed537ec39`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073e8c87a452a1089ee2f285ee9f0fd6d443ba13e37b461294a6b7c204cd11e0`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 6.2 MB (6171668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeda0333d98d2f845d4f940a65fd45cc8218c4563bf6b90bafcc56757505207`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb62a422756187601a73fc9fdc7315e65cd3b33e2a1df57ac02fc213c32d4561`  
		Last Modified: Mon, 01 Dec 2025 23:57:29 GMT  
		Size: 47.8 MB (47810641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc6f3f67d3b16b8cce7d0b84c6b87f6d986f337113312475dd57c343c308594`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:962936f2812ba266dad501074288329d0651c8246ba4199462d826c0c2dc084a`  
		Last Modified: Tue, 02 Dec 2025 01:01:21 GMT  
		Size: 130.9 MB (130926612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975113f25fa4405fa86cc427371c29944f1ff8d35ba492cf0512d5a9e09131d`  
		Last Modified: Mon, 01 Dec 2025 23:57:16 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:832545c254d04b9baf4805c0cea3e10bb5793d1a6e4f252bafaaa3a5cc5310d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14931462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a124764856093e8c488d23e12a2a32a130e25a7e7a0abdebe82671041f4a62c9`

```dockerfile
```

-	Layers:
	-	`sha256:0f59233fcd1831393794654d75e45cde1aa84dde071e9df6b2b3a1707430ed4d`  
		Last Modified: Tue, 02 Dec 2025 01:02:29 GMT  
		Size: 14.9 MB (14897254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e035f3868d177b5f73af0a04ca9cbd664ee2ed5e3fcbc51fa80a3b14a9acadc3`  
		Last Modified: Tue, 02 Dec 2025 01:02:30 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:df7c8ffeb337cbbfe1f87f6d5d3bf04196de209a99c886d24c7659921dccb1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228460405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:762c9c9acbe839ba9a5df9b1c4570b410cae6ee0fbf801758e96089b1b652048`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:03 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:05 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:05 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:29 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Dec 2025 00:00:30 GMT
ENV MYSQL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:57 GMT
ENV MYSQL_SHELL_VERSION=8.4.7-1.el9
# Tue, 02 Dec 2025 00:01:30 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:30 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:31 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:31 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b033de23cf2706769f9c4bb2cbb5b10c6099315399efbb234e4c39ce26740a9`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0f376ad4caf63cfc0d5206cd7cb08e721658906eab8d996c1c545fa9237f5`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6babe1e928a5d12942418b9eb4b1a6bee195483661127f6dde904c6277a8f0f`  
		Last Modified: Tue, 02 Dec 2025 00:02:13 GMT  
		Size: 5.8 MB (5796116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84686d2814a97e522c69cd426a1bed2fc0d6e309e2076902ee6c05b1c918ed`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81854d1b00c0c8067409b0edb96275792f7b1841c7cdb191a77feb91f2366e03`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502541f1ad7b855e6d3721aea0f23c3a2ef7a901fe513bad128e28c770c4b550`  
		Last Modified: Tue, 02 Dec 2025 00:02:16 GMT  
		Size: 46.7 MB (46693648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00295b46534d82116b9cbf44c4c24cd957b1c30951b6e9f6e0ae7e768dd387ca`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9175227a9f97f3fbd39fed46f489b57f227f998c432c4a75e4f5c2360009e0`  
		Last Modified: Tue, 02 Dec 2025 00:42:10 GMT  
		Size: 129.3 MB (129326662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:932db736281eed1032747d17cf97e29f7183d0ec8b75163109aff41021081150`  
		Last Modified: Tue, 02 Dec 2025 00:02:12 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:a7a41ae069cbadaed56707066d06c7762ed4a75b17d96c045e80f35bb4e2f9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14930185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e9a46a73df6070f21b8ba2dc27e3ae5dd5c3c604abf5bc5954e3e1d844898ce`

```dockerfile
```

-	Layers:
	-	`sha256:d360f30da8276e8028442679252da97e48bfce6e83cc37c307809b44ab17cec6`  
		Last Modified: Tue, 02 Dec 2025 01:02:40 GMT  
		Size: 14.9 MB (14895674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cde83b5870941e01c31fac5c407e7e5d1de50f46c51e6f3c52bd2e2f66466523`  
		Last Modified: Tue, 02 Dec 2025 01:02:41 GMT  
		Size: 34.5 KB (34511 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:28540698ce89bd72f985044de942d65bd99c6fadb2db105327db57f3f70564f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:dd42a451fe2a7ac18f9fbc9478c30596372cd27c2222c4cb50620338d03ee26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274726167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d568f67edbcf69c54ea79487427c32545904967c48506583f4766e787e766732`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:46:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:46:04 GMT
CMD ["/bin/bash"]
# Mon, 01 Dec 2025 23:55:21 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 01 Dec 2025 23:55:22 GMT
ENV GOSU_VERSION=1.19
# Mon, 01 Dec 2025 23:55:22 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 01 Dec 2025 23:55:45 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:55:45 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 01 Dec 2025 23:56:11 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Mon, 01 Dec 2025 23:56:47 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
VOLUME [/var/lib/mysql]
# Mon, 01 Dec 2025 23:56:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Dec 2025 23:56:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Dec 2025 23:56:47 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 01 Dec 2025 23:56:47 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:04a32ca23735c402e5cc07bceb8fa7d06ed2ca51d31dfc4e50593de0945b03dd`  
		Last Modified: Mon, 01 Dec 2025 23:46:29 GMT  
		Size: 47.3 MB (47312174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ebb6c280f32a1dfc2cb5f613ff06fc9655058e47ce2bad6c0d13d2da035f79`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9908b1bc00359c9aae93c3b9c769ee2ee12f1b1a21696f48ffe53d644567e76a`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 783.6 KB (783555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db16934d0d6e819d06f6b2cbf38d291093a463681e6e85ac330429acaf5e7fa8`  
		Last Modified: Mon, 01 Dec 2025 23:57:34 GMT  
		Size: 6.2 MB (6171583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50ff9c82874ac89550d315b633a9127b41f8c2adc1449caeef4c2aa3b86199d`  
		Last Modified: Mon, 01 Dec 2025 23:57:19 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e867246b3f6037ef3b66680fd529522051f7f583f973e7dbceeb5bb5b0f0a155`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535942d9d4859ea36596b22311a813c21c7defcca5ac911e0770608e56a27a7d`  
		Last Modified: Mon, 01 Dec 2025 23:57:38 GMT  
		Size: 51.3 MB (51336861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe13791f0771c7f09a6c5f55fb1282480fc41d18fd6bb85177a6416551006a53`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11039659ba62b150c643aebc494fa3bfabdd8e5c4175cdc105c81a747e8832d3`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 169.1 MB (169112510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8d13e504cb59db0790adc6737e2aeac761be9fd5f46a12dff48f4391d7b87`  
		Last Modified: Mon, 01 Dec 2025 23:57:33 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f435df576ad8d14dc479a4c624c7f4e762d5d41a6a073bba3455392c2584161d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.9 MB (17850295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e17b047ec75afcce73a20b56745d08ded16b02b57cc4d1d80ceffd42adbead`

```dockerfile
```

-	Layers:
	-	`sha256:281726107253b80d8c24afec196d3fb967bbba51ce136132bcb07873bd92c2ce`  
		Last Modified: Tue, 02 Dec 2025 01:03:17 GMT  
		Size: 17.8 MB (17815020 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddd72744b88618cff278d4719e7eda816d1ec29e04d9f0cc4e8c3084c39933fe`  
		Last Modified: Tue, 02 Dec 2025 01:03:18 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26805bc8977e93152ad61f620b70b87aaf6713d36e42f08ad6eb322359849465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.8 MB (269789897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae6dc43ebcc2dfbf41bc4e606bf57af93eef0de4dce44b411f30ec577a5683d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 01 Dec 2025 23:47:15 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 01 Dec 2025 23:47:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 00:00:04 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Dec 2025 00:00:06 GMT
ENV GOSU_VERSION=1.19
# Tue, 02 Dec 2025 00:00:06 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Dec 2025 00:00:30 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Dec 2025 00:00:31 GMT
ENV MYSQL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:00:31 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Dec 2025 00:00:58 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Dec 2025 00:00:59 GMT
ENV MYSQL_SHELL_VERSION=9.5.0-1.el9
# Tue, 02 Dec 2025 00:01:41 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Dec 2025 00:01:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 00:01:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 00:01:41 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Dec 2025 00:01:41 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9abb991adf3cf0a283096954ec20ae1d93d9952be697d34831c05017df92a077`  
		Last Modified: Mon, 01 Dec 2025 23:47:40 GMT  
		Size: 45.9 MB (45896977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bbd8b344977d2131957f2f00f275441274e31715dc1d1473c20b8ec67524eb`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6199e342212b84b8ef4f240bec84f21a4215246de8d514308f3c95990e19e8f0`  
		Last Modified: Tue, 02 Dec 2025 00:02:29 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585198749088ef70e67058ff70bd094344444fbfe9211714dc78aa4e98313953`  
		Last Modified: Tue, 02 Dec 2025 00:02:31 GMT  
		Size: 5.8 MB (5796160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afd93cb2f54f5ba58e374886859e031cc72622d3ecec202e10a297dac8a4873`  
		Last Modified: Tue, 02 Dec 2025 00:02:32 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944b0228f20de1366fc847ac7dd86e376ac7b58b1cf99acba420bf9f7b2c7143`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e6790a7fa3a430d20c6ad9edc7708cefba9e84f5f0a5a90a92f099da964d75`  
		Last Modified: Tue, 02 Dec 2025 00:02:37 GMT  
		Size: 50.0 MB (49959028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b134e4118a9ed82dc6a87867d0f859409fdcccbd7301cb1ef2aa6af3e4297b`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0554060e6af42f8c244b9c96788834fdbaa79f06e9864d21397ef25be14e822`  
		Last Modified: Tue, 02 Dec 2025 00:09:41 GMT  
		Size: 167.4 MB (167390718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63aaf551940125ab8fb1726f3d86414721b584566486906cbfe481da077c0c8`  
		Last Modified: Tue, 02 Dec 2025 00:02:30 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:402f11d78a6bc3f10146c41aa1fd9fd2348b303f4abeb191dec58783a8fe245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.8 MB (17845779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa3c8bf5ce62b96b1b24554d4fe819b77d4ab7c488bae2bbbc7ec2ed82f22a1`

```dockerfile
```

-	Layers:
	-	`sha256:5ed8c2c4a68789e5f36c3d3a8dfa2562bb661d11ba9cf1951e3c5a3a7c0208ff`  
		Last Modified: Tue, 02 Dec 2025 01:03:31 GMT  
		Size: 17.8 MB (17810163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5251c790224237a824a0a3199cb8907eed13a99a203660bfe0e5cfcb9a1663a3`  
		Last Modified: Tue, 02 Dec 2025 01:03:32 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
