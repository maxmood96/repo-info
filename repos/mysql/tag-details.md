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
-	[`mysql:8.0.41`](#mysql8041)
-	[`mysql:8.0.41-bookworm`](#mysql8041-bookworm)
-	[`mysql:8.0.41-debian`](#mysql8041-debian)
-	[`mysql:8.0.41-oracle`](#mysql8041-oracle)
-	[`mysql:8.0.41-oraclelinux9`](#mysql8041-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.4`](#mysql844)
-	[`mysql:8.4.4-oracle`](#mysql844-oracle)
-	[`mysql:8.4.4-oraclelinux9`](#mysql844-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.2`](#mysql92)
-	[`mysql:9.2-oracle`](#mysql92-oracle)
-	[`mysql:9.2-oraclelinux9`](#mysql92-oraclelinux9)
-	[`mysql:9.2.0`](#mysql920)
-	[`mysql:9.2.0-oracle`](#mysql920-oracle)
-	[`mysql:9.2.0-oraclelinux9`](#mysql920-oraclelinux9)
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
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:4f33388ab0a152ca309eeb70cd2e4a9a8989d5006ec2a4890d883afbffd6be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:06a422efa571e8f144ccef44d65537fd47d48647d39cdedc1a2e7a1537e8516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faa32c7d292cc0057013bb78369f1c5d380236fe3315553ac8402883bb3a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e05573c29e58583900bad982c70dfd740f18f2940e2d90a04ddf0f150de9b`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d202bd608a9277c6e7d5b8a3c64721189ca1b2111f7d4d1a397d3721377a045`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 6.9 MB (6900533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930324cdd290e662f38af3357cd4ee1074f2de3ff93a94612b89e13c0280c6bd`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e29354b231ddcabe659aa742344c62a732df1686c5e94e10ca6251f46dac3`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0710d03b24e6b1296bc15ee3a02c41eeab0d4b813162d8fbcb94185b5fa1be`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 49.6 MB (49635565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead7d3dd9cc0be4808627c6606ef6da57141cdf4bbe5d5323416f6cb5590ef69`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2712d2c86d5b7e63b7f526c57de19ccb857baeae7367735e0fe53a32287be`  
		Last Modified: Wed, 22 Jan 2025 00:28:50 GMT  
		Size: 125.3 MB (125298979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa23a8b4131bf3de8d4b0589ba4573af124414a3d60c6879390bbadb421a4e`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba6b75f842bbe65101567089f251f71d006273613902c3094e269f486e55af`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1df94ce9484fbb57e1b18cc2e211212dfb2a389fbf0ecd7fae6c46ed81cdc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dc53db1f313ea706bd0cf497c3a2141de244f8f49ed94b73a06c33bbedb84`

```dockerfile
```

-	Layers:
	-	`sha256:eb560cd2708ce026c2c112d7fbcaee16a67b542a7ba2d47938f27dd4fe46ee73`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 13.8 MB (13797329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4321dc8784e6e7b128276eb6f41d0009f67306bd5f5cead21afe26fc5ab03ca5`  
		Last Modified: Wed, 22 Jan 2025 00:28:45 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ce6919be497ade305d01310913a991243caba37ed22ea2c454d342210de458b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9ebb547671a7dd19abb8bc396b09cb648f156b9566fe46e0c62e32ab9e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24aa3b123bacac36dcf8f14a60708d4ec5f744c830e8981999c3fab8117a5f`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d19dcb787b4972e851c07c946866022ceea18cdfa3fb21dd7567b15d1c8c8`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 48.5 MB (48512959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b85b3162cf9ed9aab6edc569c613b54d67f76318d0c7cf4ca57fc6dfa8f8e`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3762fc5ce9433533c1556aaf535df15e892bcfcced25166efc58e7becab5672`  
		Last Modified: Wed, 22 Jan 2025 00:49:44 GMT  
		Size: 123.9 MB (123946125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8456bdb9b8d33569c90be330b20d5b305f38625a7127c562c7596547170c9`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf69f72eed065662764cad825444de6c2df1c5d1d849d7641daf10687cfc3c`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:6f87d7b60aa2ebb2bd38c2440ebc48193d07296cd0f808fae3fa563ddbccdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d60980f8581d9527bcad31592d791fb9c0a7d63baae05fc40788643b3c90a`

```dockerfile
```

-	Layers:
	-	`sha256:1a13f68427b3aa2e31b4a6c038805f8b830a81eb03eaec0b04b5e720d2b97dbc`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 13.8 MB (13795677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d136f6a850dd9b07b519f9c801f5ded00dbd04167d1c06bae0627693e432fa`  
		Last Modified: Wed, 22 Jan 2025 00:49:40 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:4bccbc1def6cd31ad8804ac618b8d65687c5760b8d39b8450c91203a7bd69898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:81e3111aa768924307f677847521b44d1580721b4cdd3e17b0fbd78e701838d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183280915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f645003cc3283f96e5874ee03a803baafa59c96a58d4080806ca0c8047fd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba05eccb4a3005ee1662ca9a00eaf923a6c41988b6caf1439fe0abbf967b070e`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8737fb57fe0282d942d0263eb6d7dd266fbdf7593385678c561348bf90963`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309da8559c7e634c2dbe90758f6ec6deea2ff42492297d6290278ce38996bfb3`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.4 MB (1445945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c416654debd29aa5d2068b7449967e85676edef5479936d4ffc67d39ae93132`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d1fc27cf1f40b3bed69b85ccc042f05521b44db9b4166caab9b9bdd082dfc`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 15.3 MB (15296824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5771c74a752d1233720aa0ec80ed5cd573dcfb075f79b66dae7f934eba0f687a`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1baed5db111fc49c82ab4e1cc1c34cb51b0a775de29ca7d60df7bf52515146`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d510425b1ec9e97773963efd336943c2724327c0a60a7082ab6773d08130192`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 133.9 MB (133892700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a5ee78b22779099af9d3d3297ed278fa61bb6321f325cc076f98b26843ab7`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a7fb0136598280edb868e150874d3573f89c401b5694d9518bc3f578c3e5b5`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ad7cd6f139305e980c38f448b7d510cf23484c0fb5db0018eaac4c59f784f`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:cf19f5e968eb016cfd20713d2bc6d2c84e0c3f0bd2a2350386d324e243676408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce972a1f90885b725e9a728f18650a37ae8f015897e93fd1de031816d8bdaef3`

```dockerfile
```

-	Layers:
	-	`sha256:1b075682dbd8a01ab1df362eb1359daf54a16a24ed05ee463c8d5a6280f2a713`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec3c9f3c73067cc15cfa6439e39bb4ad519f4836b70a35cb342ff7e651d841b`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:4bccbc1def6cd31ad8804ac618b8d65687c5760b8d39b8450c91203a7bd69898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:81e3111aa768924307f677847521b44d1580721b4cdd3e17b0fbd78e701838d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183280915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f645003cc3283f96e5874ee03a803baafa59c96a58d4080806ca0c8047fd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba05eccb4a3005ee1662ca9a00eaf923a6c41988b6caf1439fe0abbf967b070e`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8737fb57fe0282d942d0263eb6d7dd266fbdf7593385678c561348bf90963`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309da8559c7e634c2dbe90758f6ec6deea2ff42492297d6290278ce38996bfb3`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.4 MB (1445945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c416654debd29aa5d2068b7449967e85676edef5479936d4ffc67d39ae93132`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d1fc27cf1f40b3bed69b85ccc042f05521b44db9b4166caab9b9bdd082dfc`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 15.3 MB (15296824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5771c74a752d1233720aa0ec80ed5cd573dcfb075f79b66dae7f934eba0f687a`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1baed5db111fc49c82ab4e1cc1c34cb51b0a775de29ca7d60df7bf52515146`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d510425b1ec9e97773963efd336943c2724327c0a60a7082ab6773d08130192`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 133.9 MB (133892700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a5ee78b22779099af9d3d3297ed278fa61bb6321f325cc076f98b26843ab7`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a7fb0136598280edb868e150874d3573f89c401b5694d9518bc3f578c3e5b5`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ad7cd6f139305e980c38f448b7d510cf23484c0fb5db0018eaac4c59f784f`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:cf19f5e968eb016cfd20713d2bc6d2c84e0c3f0bd2a2350386d324e243676408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce972a1f90885b725e9a728f18650a37ae8f015897e93fd1de031816d8bdaef3`

```dockerfile
```

-	Layers:
	-	`sha256:1b075682dbd8a01ab1df362eb1359daf54a16a24ed05ee463c8d5a6280f2a713`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec3c9f3c73067cc15cfa6439e39bb4ad519f4836b70a35cb342ff7e651d841b`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:4f33388ab0a152ca309eeb70cd2e4a9a8989d5006ec2a4890d883afbffd6be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06a422efa571e8f144ccef44d65537fd47d48647d39cdedc1a2e7a1537e8516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faa32c7d292cc0057013bb78369f1c5d380236fe3315553ac8402883bb3a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e05573c29e58583900bad982c70dfd740f18f2940e2d90a04ddf0f150de9b`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d202bd608a9277c6e7d5b8a3c64721189ca1b2111f7d4d1a397d3721377a045`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 6.9 MB (6900533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930324cdd290e662f38af3357cd4ee1074f2de3ff93a94612b89e13c0280c6bd`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e29354b231ddcabe659aa742344c62a732df1686c5e94e10ca6251f46dac3`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0710d03b24e6b1296bc15ee3a02c41eeab0d4b813162d8fbcb94185b5fa1be`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 49.6 MB (49635565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead7d3dd9cc0be4808627c6606ef6da57141cdf4bbe5d5323416f6cb5590ef69`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2712d2c86d5b7e63b7f526c57de19ccb857baeae7367735e0fe53a32287be`  
		Last Modified: Wed, 22 Jan 2025 00:28:50 GMT  
		Size: 125.3 MB (125298979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa23a8b4131bf3de8d4b0589ba4573af124414a3d60c6879390bbadb421a4e`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba6b75f842bbe65101567089f251f71d006273613902c3094e269f486e55af`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1df94ce9484fbb57e1b18cc2e211212dfb2a389fbf0ecd7fae6c46ed81cdc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dc53db1f313ea706bd0cf497c3a2141de244f8f49ed94b73a06c33bbedb84`

```dockerfile
```

-	Layers:
	-	`sha256:eb560cd2708ce026c2c112d7fbcaee16a67b542a7ba2d47938f27dd4fe46ee73`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 13.8 MB (13797329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4321dc8784e6e7b128276eb6f41d0009f67306bd5f5cead21afe26fc5ab03ca5`  
		Last Modified: Wed, 22 Jan 2025 00:28:45 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ce6919be497ade305d01310913a991243caba37ed22ea2c454d342210de458b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9ebb547671a7dd19abb8bc396b09cb648f156b9566fe46e0c62e32ab9e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24aa3b123bacac36dcf8f14a60708d4ec5f744c830e8981999c3fab8117a5f`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d19dcb787b4972e851c07c946866022ceea18cdfa3fb21dd7567b15d1c8c8`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 48.5 MB (48512959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b85b3162cf9ed9aab6edc569c613b54d67f76318d0c7cf4ca57fc6dfa8f8e`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3762fc5ce9433533c1556aaf535df15e892bcfcced25166efc58e7becab5672`  
		Last Modified: Wed, 22 Jan 2025 00:49:44 GMT  
		Size: 123.9 MB (123946125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8456bdb9b8d33569c90be330b20d5b305f38625a7127c562c7596547170c9`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf69f72eed065662764cad825444de6c2df1c5d1d849d7641daf10687cfc3c`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6f87d7b60aa2ebb2bd38c2440ebc48193d07296cd0f808fae3fa563ddbccdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d60980f8581d9527bcad31592d791fb9c0a7d63baae05fc40788643b3c90a`

```dockerfile
```

-	Layers:
	-	`sha256:1a13f68427b3aa2e31b4a6c038805f8b830a81eb03eaec0b04b5e720d2b97dbc`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 13.8 MB (13795677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d136f6a850dd9b07b519f9c801f5ded00dbd04167d1c06bae0627693e432fa`  
		Last Modified: Wed, 22 Jan 2025 00:49:40 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:4f33388ab0a152ca309eeb70cd2e4a9a8989d5006ec2a4890d883afbffd6be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06a422efa571e8f144ccef44d65537fd47d48647d39cdedc1a2e7a1537e8516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faa32c7d292cc0057013bb78369f1c5d380236fe3315553ac8402883bb3a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e05573c29e58583900bad982c70dfd740f18f2940e2d90a04ddf0f150de9b`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d202bd608a9277c6e7d5b8a3c64721189ca1b2111f7d4d1a397d3721377a045`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 6.9 MB (6900533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930324cdd290e662f38af3357cd4ee1074f2de3ff93a94612b89e13c0280c6bd`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e29354b231ddcabe659aa742344c62a732df1686c5e94e10ca6251f46dac3`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0710d03b24e6b1296bc15ee3a02c41eeab0d4b813162d8fbcb94185b5fa1be`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 49.6 MB (49635565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead7d3dd9cc0be4808627c6606ef6da57141cdf4bbe5d5323416f6cb5590ef69`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2712d2c86d5b7e63b7f526c57de19ccb857baeae7367735e0fe53a32287be`  
		Last Modified: Wed, 22 Jan 2025 00:28:50 GMT  
		Size: 125.3 MB (125298979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa23a8b4131bf3de8d4b0589ba4573af124414a3d60c6879390bbadb421a4e`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba6b75f842bbe65101567089f251f71d006273613902c3094e269f486e55af`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1df94ce9484fbb57e1b18cc2e211212dfb2a389fbf0ecd7fae6c46ed81cdc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dc53db1f313ea706bd0cf497c3a2141de244f8f49ed94b73a06c33bbedb84`

```dockerfile
```

-	Layers:
	-	`sha256:eb560cd2708ce026c2c112d7fbcaee16a67b542a7ba2d47938f27dd4fe46ee73`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 13.8 MB (13797329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4321dc8784e6e7b128276eb6f41d0009f67306bd5f5cead21afe26fc5ab03ca5`  
		Last Modified: Wed, 22 Jan 2025 00:28:45 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ce6919be497ade305d01310913a991243caba37ed22ea2c454d342210de458b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9ebb547671a7dd19abb8bc396b09cb648f156b9566fe46e0c62e32ab9e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24aa3b123bacac36dcf8f14a60708d4ec5f744c830e8981999c3fab8117a5f`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d19dcb787b4972e851c07c946866022ceea18cdfa3fb21dd7567b15d1c8c8`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 48.5 MB (48512959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b85b3162cf9ed9aab6edc569c613b54d67f76318d0c7cf4ca57fc6dfa8f8e`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3762fc5ce9433533c1556aaf535df15e892bcfcced25166efc58e7becab5672`  
		Last Modified: Wed, 22 Jan 2025 00:49:44 GMT  
		Size: 123.9 MB (123946125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8456bdb9b8d33569c90be330b20d5b305f38625a7127c562c7596547170c9`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf69f72eed065662764cad825444de6c2df1c5d1d849d7641daf10687cfc3c`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6f87d7b60aa2ebb2bd38c2440ebc48193d07296cd0f808fae3fa563ddbccdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d60980f8581d9527bcad31592d791fb9c0a7d63baae05fc40788643b3c90a`

```dockerfile
```

-	Layers:
	-	`sha256:1a13f68427b3aa2e31b4a6c038805f8b830a81eb03eaec0b04b5e720d2b97dbc`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 13.8 MB (13795677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d136f6a850dd9b07b519f9c801f5ded00dbd04167d1c06bae0627693e432fa`  
		Last Modified: Wed, 22 Jan 2025 00:49:40 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41`

```console
$ docker pull mysql@sha256:4f33388ab0a152ca309eeb70cd2e4a9a8989d5006ec2a4890d883afbffd6be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41` - linux; amd64

```console
$ docker pull mysql@sha256:06a422efa571e8f144ccef44d65537fd47d48647d39cdedc1a2e7a1537e8516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faa32c7d292cc0057013bb78369f1c5d380236fe3315553ac8402883bb3a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e05573c29e58583900bad982c70dfd740f18f2940e2d90a04ddf0f150de9b`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d202bd608a9277c6e7d5b8a3c64721189ca1b2111f7d4d1a397d3721377a045`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 6.9 MB (6900533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930324cdd290e662f38af3357cd4ee1074f2de3ff93a94612b89e13c0280c6bd`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e29354b231ddcabe659aa742344c62a732df1686c5e94e10ca6251f46dac3`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0710d03b24e6b1296bc15ee3a02c41eeab0d4b813162d8fbcb94185b5fa1be`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 49.6 MB (49635565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead7d3dd9cc0be4808627c6606ef6da57141cdf4bbe5d5323416f6cb5590ef69`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2712d2c86d5b7e63b7f526c57de19ccb857baeae7367735e0fe53a32287be`  
		Last Modified: Wed, 22 Jan 2025 00:28:50 GMT  
		Size: 125.3 MB (125298979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa23a8b4131bf3de8d4b0589ba4573af124414a3d60c6879390bbadb421a4e`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba6b75f842bbe65101567089f251f71d006273613902c3094e269f486e55af`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:1df94ce9484fbb57e1b18cc2e211212dfb2a389fbf0ecd7fae6c46ed81cdc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dc53db1f313ea706bd0cf497c3a2141de244f8f49ed94b73a06c33bbedb84`

```dockerfile
```

-	Layers:
	-	`sha256:eb560cd2708ce026c2c112d7fbcaee16a67b542a7ba2d47938f27dd4fe46ee73`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 13.8 MB (13797329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4321dc8784e6e7b128276eb6f41d0009f67306bd5f5cead21afe26fc5ab03ca5`  
		Last Modified: Wed, 22 Jan 2025 00:28:45 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ce6919be497ade305d01310913a991243caba37ed22ea2c454d342210de458b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9ebb547671a7dd19abb8bc396b09cb648f156b9566fe46e0c62e32ab9e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24aa3b123bacac36dcf8f14a60708d4ec5f744c830e8981999c3fab8117a5f`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d19dcb787b4972e851c07c946866022ceea18cdfa3fb21dd7567b15d1c8c8`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 48.5 MB (48512959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b85b3162cf9ed9aab6edc569c613b54d67f76318d0c7cf4ca57fc6dfa8f8e`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3762fc5ce9433533c1556aaf535df15e892bcfcced25166efc58e7becab5672`  
		Last Modified: Wed, 22 Jan 2025 00:49:44 GMT  
		Size: 123.9 MB (123946125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8456bdb9b8d33569c90be330b20d5b305f38625a7127c562c7596547170c9`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf69f72eed065662764cad825444de6c2df1c5d1d849d7641daf10687cfc3c`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41` - unknown; unknown

```console
$ docker pull mysql@sha256:6f87d7b60aa2ebb2bd38c2440ebc48193d07296cd0f808fae3fa563ddbccdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d60980f8581d9527bcad31592d791fb9c0a7d63baae05fc40788643b3c90a`

```dockerfile
```

-	Layers:
	-	`sha256:1a13f68427b3aa2e31b4a6c038805f8b830a81eb03eaec0b04b5e720d2b97dbc`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 13.8 MB (13795677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d136f6a850dd9b07b519f9c801f5ded00dbd04167d1c06bae0627693e432fa`  
		Last Modified: Wed, 22 Jan 2025 00:49:40 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-bookworm`

```console
$ docker pull mysql@sha256:4bccbc1def6cd31ad8804ac618b8d65687c5760b8d39b8450c91203a7bd69898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:81e3111aa768924307f677847521b44d1580721b4cdd3e17b0fbd78e701838d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183280915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f645003cc3283f96e5874ee03a803baafa59c96a58d4080806ca0c8047fd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba05eccb4a3005ee1662ca9a00eaf923a6c41988b6caf1439fe0abbf967b070e`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8737fb57fe0282d942d0263eb6d7dd266fbdf7593385678c561348bf90963`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309da8559c7e634c2dbe90758f6ec6deea2ff42492297d6290278ce38996bfb3`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.4 MB (1445945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c416654debd29aa5d2068b7449967e85676edef5479936d4ffc67d39ae93132`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d1fc27cf1f40b3bed69b85ccc042f05521b44db9b4166caab9b9bdd082dfc`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 15.3 MB (15296824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5771c74a752d1233720aa0ec80ed5cd573dcfb075f79b66dae7f934eba0f687a`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1baed5db111fc49c82ab4e1cc1c34cb51b0a775de29ca7d60df7bf52515146`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d510425b1ec9e97773963efd336943c2724327c0a60a7082ab6773d08130192`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 133.9 MB (133892700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a5ee78b22779099af9d3d3297ed278fa61bb6321f325cc076f98b26843ab7`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a7fb0136598280edb868e150874d3573f89c401b5694d9518bc3f578c3e5b5`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ad7cd6f139305e980c38f448b7d510cf23484c0fb5db0018eaac4c59f784f`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:cf19f5e968eb016cfd20713d2bc6d2c84e0c3f0bd2a2350386d324e243676408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce972a1f90885b725e9a728f18650a37ae8f015897e93fd1de031816d8bdaef3`

```dockerfile
```

-	Layers:
	-	`sha256:1b075682dbd8a01ab1df362eb1359daf54a16a24ed05ee463c8d5a6280f2a713`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec3c9f3c73067cc15cfa6439e39bb4ad519f4836b70a35cb342ff7e651d841b`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-debian`

```console
$ docker pull mysql@sha256:4bccbc1def6cd31ad8804ac618b8d65687c5760b8d39b8450c91203a7bd69898
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.41-debian` - linux; amd64

```console
$ docker pull mysql@sha256:81e3111aa768924307f677847521b44d1580721b4cdd3e17b0fbd78e701838d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183280915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1f645003cc3283f96e5874ee03a803baafa59c96a58d4080806ca0c8047fd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Tue, 21 Jan 2025 17:15:14 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1debian12
# Tue, 21 Jan 2025 17:15:14 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba05eccb4a3005ee1662ca9a00eaf923a6c41988b6caf1439fe0abbf967b070e`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a8737fb57fe0282d942d0263eb6d7dd266fbdf7593385678c561348bf90963`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.4 MB (4422758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309da8559c7e634c2dbe90758f6ec6deea2ff42492297d6290278ce38996bfb3`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 1.4 MB (1445945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c416654debd29aa5d2068b7449967e85676edef5479936d4ffc67d39ae93132`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806d1fc27cf1f40b3bed69b85ccc042f05521b44db9b4166caab9b9bdd082dfc`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 15.3 MB (15296824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5771c74a752d1233720aa0ec80ed5cd573dcfb075f79b66dae7f934eba0f687a`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 2.5 KB (2506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd1baed5db111fc49c82ab4e1cc1c34cb51b0a775de29ca7d60df7bf52515146`  
		Last Modified: Wed, 22 Jan 2025 00:27:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d510425b1ec9e97773963efd336943c2724327c0a60a7082ab6773d08130192`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 133.9 MB (133892700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2a5ee78b22779099af9d3d3297ed278fa61bb6321f325cc076f98b26843ab7`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a7fb0136598280edb868e150874d3573f89c401b5694d9518bc3f578c3e5b5`  
		Last Modified: Wed, 22 Jan 2025 00:27:54 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9ad7cd6f139305e980c38f448b7d510cf23484c0fb5db0018eaac4c59f784f`  
		Last Modified: Wed, 22 Jan 2025 00:27:55 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:cf19f5e968eb016cfd20713d2bc6d2c84e0c3f0bd2a2350386d324e243676408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce972a1f90885b725e9a728f18650a37ae8f015897e93fd1de031816d8bdaef3`

```dockerfile
```

-	Layers:
	-	`sha256:1b075682dbd8a01ab1df362eb1359daf54a16a24ed05ee463c8d5a6280f2a713`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ec3c9f3c73067cc15cfa6439e39bb4ad519f4836b70a35cb342ff7e651d841b`  
		Last Modified: Wed, 22 Jan 2025 00:27:52 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oracle`

```console
$ docker pull mysql@sha256:4f33388ab0a152ca309eeb70cd2e4a9a8989d5006ec2a4890d883afbffd6be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06a422efa571e8f144ccef44d65537fd47d48647d39cdedc1a2e7a1537e8516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faa32c7d292cc0057013bb78369f1c5d380236fe3315553ac8402883bb3a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e05573c29e58583900bad982c70dfd740f18f2940e2d90a04ddf0f150de9b`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d202bd608a9277c6e7d5b8a3c64721189ca1b2111f7d4d1a397d3721377a045`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 6.9 MB (6900533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930324cdd290e662f38af3357cd4ee1074f2de3ff93a94612b89e13c0280c6bd`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e29354b231ddcabe659aa742344c62a732df1686c5e94e10ca6251f46dac3`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0710d03b24e6b1296bc15ee3a02c41eeab0d4b813162d8fbcb94185b5fa1be`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 49.6 MB (49635565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead7d3dd9cc0be4808627c6606ef6da57141cdf4bbe5d5323416f6cb5590ef69`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2712d2c86d5b7e63b7f526c57de19ccb857baeae7367735e0fe53a32287be`  
		Last Modified: Wed, 22 Jan 2025 00:28:50 GMT  
		Size: 125.3 MB (125298979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa23a8b4131bf3de8d4b0589ba4573af124414a3d60c6879390bbadb421a4e`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba6b75f842bbe65101567089f251f71d006273613902c3094e269f486e55af`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1df94ce9484fbb57e1b18cc2e211212dfb2a389fbf0ecd7fae6c46ed81cdc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dc53db1f313ea706bd0cf497c3a2141de244f8f49ed94b73a06c33bbedb84`

```dockerfile
```

-	Layers:
	-	`sha256:eb560cd2708ce026c2c112d7fbcaee16a67b542a7ba2d47938f27dd4fe46ee73`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 13.8 MB (13797329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4321dc8784e6e7b128276eb6f41d0009f67306bd5f5cead21afe26fc5ab03ca5`  
		Last Modified: Wed, 22 Jan 2025 00:28:45 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ce6919be497ade305d01310913a991243caba37ed22ea2c454d342210de458b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9ebb547671a7dd19abb8bc396b09cb648f156b9566fe46e0c62e32ab9e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24aa3b123bacac36dcf8f14a60708d4ec5f744c830e8981999c3fab8117a5f`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d19dcb787b4972e851c07c946866022ceea18cdfa3fb21dd7567b15d1c8c8`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 48.5 MB (48512959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b85b3162cf9ed9aab6edc569c613b54d67f76318d0c7cf4ca57fc6dfa8f8e`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3762fc5ce9433533c1556aaf535df15e892bcfcced25166efc58e7becab5672`  
		Last Modified: Wed, 22 Jan 2025 00:49:44 GMT  
		Size: 123.9 MB (123946125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8456bdb9b8d33569c90be330b20d5b305f38625a7127c562c7596547170c9`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf69f72eed065662764cad825444de6c2df1c5d1d849d7641daf10687cfc3c`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:6f87d7b60aa2ebb2bd38c2440ebc48193d07296cd0f808fae3fa563ddbccdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d60980f8581d9527bcad31592d791fb9c0a7d63baae05fc40788643b3c90a`

```dockerfile
```

-	Layers:
	-	`sha256:1a13f68427b3aa2e31b4a6c038805f8b830a81eb03eaec0b04b5e720d2b97dbc`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 13.8 MB (13795677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d136f6a850dd9b07b519f9c801f5ded00dbd04167d1c06bae0627693e432fa`  
		Last Modified: Wed, 22 Jan 2025 00:49:40 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.41-oraclelinux9`

```console
$ docker pull mysql@sha256:4f33388ab0a152ca309eeb70cd2e4a9a8989d5006ec2a4890d883afbffd6be4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.41-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06a422efa571e8f144ccef44d65537fd47d48647d39cdedc1a2e7a1537e8516e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231926373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04faa32c7d292cc0057013bb78369f1c5d380236fe3315553ac8402883bb3a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e05573c29e58583900bad982c70dfd740f18f2940e2d90a04ddf0f150de9b`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d202bd608a9277c6e7d5b8a3c64721189ca1b2111f7d4d1a397d3721377a045`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 6.9 MB (6900533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930324cdd290e662f38af3357cd4ee1074f2de3ff93a94612b89e13c0280c6bd`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:441e29354b231ddcabe659aa742344c62a732df1686c5e94e10ca6251f46dac3`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0710d03b24e6b1296bc15ee3a02c41eeab0d4b813162d8fbcb94185b5fa1be`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 49.6 MB (49635565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead7d3dd9cc0be4808627c6606ef6da57141cdf4bbe5d5323416f6cb5590ef69`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55d2712d2c86d5b7e63b7f526c57de19ccb857baeae7367735e0fe53a32287be`  
		Last Modified: Wed, 22 Jan 2025 00:28:50 GMT  
		Size: 125.3 MB (125298979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaa23a8b4131bf3de8d4b0589ba4573af124414a3d60c6879390bbadb421a4e`  
		Last Modified: Wed, 22 Jan 2025 00:28:47 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ba6b75f842bbe65101567089f251f71d006273613902c3094e269f486e55af`  
		Last Modified: Wed, 22 Jan 2025 00:28:48 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1df94ce9484fbb57e1b18cc2e211212dfb2a389fbf0ecd7fae6c46ed81cdc923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13832283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3dc53db1f313ea706bd0cf497c3a2141de244f8f49ed94b73a06c33bbedb84`

```dockerfile
```

-	Layers:
	-	`sha256:eb560cd2708ce026c2c112d7fbcaee16a67b542a7ba2d47938f27dd4fe46ee73`  
		Last Modified: Wed, 22 Jan 2025 00:28:46 GMT  
		Size: 13.8 MB (13797329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4321dc8784e6e7b128276eb6f41d0009f67306bd5f5cead21afe26fc5ab03ca5`  
		Last Modified: Wed, 22 Jan 2025 00:28:45 GMT  
		Size: 35.0 KB (34954 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.41-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ce6919be497ade305d01310913a991243caba37ed22ea2c454d342210de458b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227546116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28a9ebb547671a7dd19abb8bc396b09cb648f156b9566fe46e0c62e32ab9e200`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENV MYSQL_SHELL_VERSION=8.0.41-1.el9
# Tue, 21 Jan 2025 17:15:14 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:15:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 21 Jan 2025 17:15:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:15:14 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:15:14 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c24aa3b123bacac36dcf8f14a60708d4ec5f744c830e8981999c3fab8117a5f`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273d19dcb787b4972e851c07c946866022ceea18cdfa3fb21dd7567b15d1c8c8`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 48.5 MB (48512959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144b85b3162cf9ed9aab6edc569c613b54d67f76318d0c7cf4ca57fc6dfa8f8e`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3762fc5ce9433533c1556aaf535df15e892bcfcced25166efc58e7becab5672`  
		Last Modified: Wed, 22 Jan 2025 00:49:44 GMT  
		Size: 123.9 MB (123946125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b8456bdb9b8d33569c90be330b20d5b305f38625a7127c562c7596547170c9`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1baf69f72eed065662764cad825444de6c2df1c5d1d849d7641daf10687cfc3c`  
		Last Modified: Wed, 22 Jan 2025 00:49:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.41-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:6f87d7b60aa2ebb2bd38c2440ebc48193d07296cd0f808fae3fa563ddbccdcc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13830879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7d60980f8581d9527bcad31592d791fb9c0a7d63baae05fc40788643b3c90a`

```dockerfile
```

-	Layers:
	-	`sha256:1a13f68427b3aa2e31b4a6c038805f8b830a81eb03eaec0b04b5e720d2b97dbc`  
		Last Modified: Wed, 22 Jan 2025 00:49:41 GMT  
		Size: 13.8 MB (13795677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9d136f6a850dd9b07b519f9c801f5ded00dbd04167d1c06bae0627693e432fa`  
		Last Modified: Wed, 22 Jan 2025 00:49:40 GMT  
		Size: 35.2 KB (35202 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oracle`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.4-oraclelinux9`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oracle`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2-oraclelinux9`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oracle`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.2.0-oraclelinux9`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.2.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.2.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.2.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:1d967fb75a64dc3c2894c69285becfc2304ae0c3c4f4c715c297f3c12d60b01c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:78d25f90357c78b4784dad586c97edaba3654c330d9b2af0095e5fea630932eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.9 MB (232926997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0934992dec280f1937e76a478fbcf665f9d559462af799c594d3bea1409a0de6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb40fda03e3d771dae07c3a61b170139e20565ae8079f1f269afb34a7359bc7`  
		Last Modified: Wed, 22 Jan 2025 00:29:58 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6c73d8c7a7af55eecef58037873acb92622548708d25fbf249679e861cdc95`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986789341eb6cdca7697a7af7c440c8d7c4fd41147afa1b355b679018beffd14`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 6.9 MB (6900482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720920ea2b0be1c2a18741fa3ad096d206d6f70640a95576a3b35bbe2a2a50d9`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8789191db836ed0112a34aaefa8f00633606248ca4d09ace4a0be54f78ea01a8`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311a2cd705b01b8ee234432769e2ab1ddec25a5cfccca8b39e97ab808329faba`  
		Last Modified: Wed, 22 Jan 2025 00:30:01 GMT  
		Size: 47.6 MB (47595422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3883debd05a31e45aec7648ba822046ba2b2c883f99aabdf873978797c0a4aa1`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdca1d64207db8bb46e4388863ac15c533679c42cc9e131379388b2ea5723ee9`  
		Last Modified: Wed, 22 Jan 2025 00:30:04 GMT  
		Size: 128.3 MB (128339917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add1d61b6f4b51d8b4bbb257b478fd1df8393344df8a9e5ab50bd28e48b7334`  
		Last Modified: Wed, 22 Jan 2025 00:30:00 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:64b0bad5d331b1d757e959e621afd90a92144ff4db0bc73dafb2ca76dd22ab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14108401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04b0d45d28e140f0134371ec96e3ce531b3e5c36a21d3f556ffc35a11f4f903`

```dockerfile
```

-	Layers:
	-	`sha256:5866b717b83a9cc9a27b896099871ffddc367d74a731a0dd41a619b5ec61e8f6`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 14.1 MB (14074150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7dcbad5696e79088320c89ced3b27858f179eaa9a3bc64205d81c60fe72db62`  
		Last Modified: Wed, 22 Jan 2025 00:29:59 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:291caa9566f9c3ce9542ee8b8b4589a387c8faff87f823c0fc55ec7a641a46c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228367538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c462b1ee6af165b0170062d4a7d9cc8f4bb3bc49e37148f7a21bc66ae415e810`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENV MYSQL_SHELL_VERSION=8.4.4-1.el9
# Tue, 21 Jan 2025 17:21:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:21:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:21:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:21:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:21:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2668a8281b7268fc08552f80ac15fe7a907162ecf83c4e27b9e1d3506d9b7f`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd440e2669c30223762fccaede52a073eef4eed390ab47e95c720f01b739de5`  
		Last Modified: Wed, 22 Jan 2025 00:48:11 GMT  
		Size: 46.5 MB (46473799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6a9cf642cf7c9f1f9238d7de08af3c27a99107d76ab0ef571fa8ad57607c4`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e521efae22b3d8724111606ed460fbef331eb32c8355cdf6d0543a0962cdb217`  
		Last Modified: Wed, 22 Jan 2025 00:48:13 GMT  
		Size: 126.8 MB (126806819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:babc7aaaa09592c1d44f4aeb00c66ead5dd2e22f8536d64fa021b12ecab0a5cf`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 5.3 KB (5335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4dac0a419214e5c5e58ebe18d899f96b301c1881f5cac9b5e5e20fb16276a114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.1 MB (14107126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c0a6d8e61429ec7f0d88682c38198daac2ed2d597c047ada6fa5bae8c638fe8`

```dockerfile
```

-	Layers:
	-	`sha256:762564259ffcf01bd7760b9d54fc58b5ca55495ca8a53d334029b2a6a26da8f5`  
		Last Modified: Wed, 22 Jan 2025 00:48:10 GMT  
		Size: 14.1 MB (14072570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33b2d4a5e8b74d620ba5592165958a08e4641e9358d11fcf0eba76cf0b756405`  
		Last Modified: Wed, 22 Jan 2025 00:48:09 GMT  
		Size: 34.6 KB (34556 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:e863828bfad034b8848d37640d7ed95746849c9ebc026a4abf2ca3d85b0a450e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:09f5f336fa30ead3529d829eac31a2d1c4dbf405f7784e40a495d8faac8b0cd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174502891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c247418d4e065cb75e18acf7ccc8fce8a6aa0138a580b57dd023918b5ef2ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb027c65a85cfe71e10cb49319c0786a090eb22468ca3422c214c88de3ae3c20`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0747a4bff6cc331618078318c1bca51d994163a1174334dcb716867a7b4041`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a67d6d40a5b95ff4c8a8b509a3c40bd4575f93b00c84677478cb6decbacffb2`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 6.9 MB (6900524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c572287499e73d10b7c9fff505b7503a00188477fe54c25b10d236b86c998c`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d7b1770f6b612b6a695b15160d3e30b9220fc92964de151cbfc3ec057c2a72`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5086dfc014b63f301004e0818fd180de81c391656c2d24f163e4c156e87eb707`  
		Last Modified: Wed, 22 Jan 2025 00:28:37 GMT  
		Size: 48.4 MB (48429481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0f55b762fd39ee61a76784636ce96615124adb61271bfd6253518847a62a0`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd6c85e2555dc0907be4593c8cbb5c9f0b57804e4f17fbd61d6df6596da225`  
		Last Modified: Wed, 22 Jan 2025 00:28:38 GMT  
		Size: 69.1 MB (69081697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9a54c9e55ed4d4edc5ee1fa81529402cad99b650dedfb0b27baf62cd2b9f34`  
		Last Modified: Wed, 22 Jan 2025 00:28:36 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3e9943b04b4dc0801f711f85e98d0336c8717425198540ddc5665570c7b09a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14888275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe907972076d812302eb290abe59424ca2ffe3b4cdde9d9a8db1484d649f9f02`

```dockerfile
```

-	Layers:
	-	`sha256:3a13ea9355f3ecc855794464f67585d901786a91c76891c06d830a1a6f26c619`  
		Last Modified: Wed, 22 Jan 2025 00:28:35 GMT  
		Size: 14.9 MB (14852959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff9b4a37304dd62952eb2b17013941ad0ad64b8c598220de2ed19d5f39006bc7`  
		Last Modified: Wed, 22 Jan 2025 00:28:34 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:7cb6876a4331d85fc67b8bfe3a95f3ee979cd1923b60bcc4b0c41e04c8e82012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.7 MB (171684094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edd45ee6da2e3972b0c37a00b313ee8101ed2ba99878c2a18a05f725dfe1c58b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_VERSION=9.2.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Tue, 21 Jan 2025 17:25:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 21 Jan 2025 17:25:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Jan 2025 17:25:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Jan 2025 17:25:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 21 Jan 2025 17:25:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ebfd74dcb5b7f093b013a8111d1903f13c79ed5c92ad2c956cf0e32e97e75f`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08c5512fe2f397e73fe08b22d175b1f9302bde2d289dbc819bef7dc74f5a9cd`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 913.5 KB (913456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe89fd72816f51b76b2e7f6d53bbf3459ebed39c6964c869c28aebf4e00d71c`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 6.5 MB (6496589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3cf76a534ab5e054d760607b236a2cf856dcd864c7b43d29cc180c11944573`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcabec7fc12d61851b5abb2f7409f52aac6bfa4d1bfab43393f87ce6939b04b`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886685c1f09c1546856088f46790451631e2cd78c89642cef3e7096f842d7a97`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 47.3 MB (47302449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515829a0f5f2f6b338de123ebe53680811f33b9f9eb7771c672d47b170d95cfe`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f10ba4c4b2d21ad73f50bdcce8c7a26033528158fbba741a590d7a3175a40f`  
		Last Modified: Wed, 22 Jan 2025 00:46:33 GMT  
		Size: 69.3 MB (69294715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e14daf14dcc590efe6c9bbb088b2d4938b9d6786b89b24936665544abdae13f`  
		Last Modified: Wed, 22 Jan 2025 00:46:31 GMT  
		Size: 5.3 KB (5334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:31526040febdfc3691be5be9204f210fdae5c47ceb741cf1f7240c9cb3a2e9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14883849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2830a7cce4db7468da432ec7612f1c2c1d7b694b26d3ba2c7607317c07122432`

```dockerfile
```

-	Layers:
	-	`sha256:6fce2d01323fbf5e98259ba9270fe4573fb80a992f8a457d92c915ab8d38bf95`  
		Last Modified: Wed, 22 Jan 2025 00:46:30 GMT  
		Size: 14.8 MB (14848193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2a8a19c343ec8207f00acc4046a32cf9840f32ea28b77bc5eb3aa4e9b840bfd`  
		Last Modified: Wed, 22 Jan 2025 00:46:29 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json
