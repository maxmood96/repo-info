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
-	[`mysql:8.0.40`](#mysql8040)
-	[`mysql:8.0.40-bookworm`](#mysql8040-bookworm)
-	[`mysql:8.0.40-debian`](#mysql8040-debian)
-	[`mysql:8.0.40-oracle`](#mysql8040-oracle)
-	[`mysql:8.0.40-oraclelinux9`](#mysql8040-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.3`](#mysql843)
-	[`mysql:8.4.3-oracle`](#mysql843-oracle)
-	[`mysql:8.4.3-oraclelinux9`](#mysql843-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.1`](#mysql91)
-	[`mysql:9.1-oracle`](#mysql91-oracle)
-	[`mysql:9.1-oraclelinux9`](#mysql91-oraclelinux9)
-	[`mysql:9.1.0`](#mysql910)
-	[`mysql:9.1.0-oracle`](#mysql910-oracle)
-	[`mysql:9.1.0-oraclelinux9`](#mysql910-oraclelinux9)
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
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:d58ac93387f644e4e040c636b8f50494e78e5afc27ca0a87348b2f577da2b7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:ed04aca46b6fe0bdc192becc17d358b46eeb82762b81ee65b80feff3d0873e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170967197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ddbef96911f9f36d1330ffe3f7557c019d49434e738cafabd1a3dd6b4bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746eccf8a0b2af211ab4e965605b2b0650135c559d7afbd8f52b462ace2044b`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d84c48f09d9af270fc8f646b8bbb4527be9af06a10ff2e2d602170036d6f51`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 6.9 MB (6900505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf1ccdd2a47cdbf9c4e42d5ca84f2e3613ee3b362ff84ec757dfad6257f72`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331406986f7012797f213303269b9a4848d879ea3bce49e761b9e0c72e4b5c8`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93598758d10e9e2a9001d29377e0117a3327b7d98dabf670202dc40152aa12c`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 49.6 MB (49616694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c136cb242f20f30b1941cdc2501f981755dae69945f60c417fb3569f5c624b9`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d476cd3429082fc815bde25dc63bfc25061d88441248702ef10a4b05525a`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 64.4 MB (64358700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe60d9fe24a9f2a8a99eeb533a302e7ac771f498e1b28589006b35987e30f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9659be67bd393aa4bf61a8b7c708b4101e9ca8bbcf5ccc4e0aba3b86e166f`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:5b82a914b82ea05e740eed150958fe1a7f6d630e32cf2b8dae901f934a8ab7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c8e4cdf3318556f4237a0acd8e65737743e64173f3813bac2a1bd76fa28e8`

```dockerfile
```

-	Layers:
	-	`sha256:a0c4224cdd564e99931920bb22cb968a9924b61182bb9cfbb22c7d4f7c9ce010`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 14.8 MB (14764257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d5c465880406594d1a711f3b62ad657d6852a73721958811351761fa0c1626`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 35.0 KB (34951 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8f440d72abf5fe4b62b257bd2eeafcd44876502e6475b4b9561c35e10fe174f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7cfd1cb86c0741bf55f72560ce6d7799ada94a51f8f192a4d3b689b8496b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683c13940f4ef84a4ff1d4011acef7afdf25ab72317c6eb9b598d99d19fea9`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673fd082ece791ba0f592b131bfdf501d5253fdb4c9dbb8edfa3e0b98f28451`  
		Last Modified: Fri, 22 Nov 2024 05:12:07 GMT  
		Size: 48.5 MB (48487316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6bb492aeb500bcb7145005a8de7a00d65f53abcb65d488ff913809ee5d28e`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928800192ffcde5c4412ef90a10b6e09e646ecca7a2be487c3a73177c99dcc1`  
		Last Modified: Fri, 22 Nov 2024 05:12:08 GMT  
		Size: 71.9 MB (71907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e587e2fcdbcdb874fcb537f5f92bf9e51f032d0df18b282d5bad6f6d83bf3e`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b3ed369b19e67e114654100f91f405ed6c08b1c0b125df65437f5cc0c2152`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:8dda4e2465a333987c039420ccd029467a9f0506cf47e2cec741f33c47493753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d4e0f0ac833d92e7a335f89561d45c881a0d9323b2b7ae42aed81e1b60342c`

```dockerfile
```

-	Layers:
	-	`sha256:65a87b45491c89738a6e29c2753f9935e039671e180484a9b85a7a666005f9c7`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 14.8 MB (14759335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6da332c7762246e5423d90bbbee6dcc72800c4471ef8b299f5e79221626dd`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:6559780c6418602460bd4087f0e0270273ee9fb12a9c7a9291bd71b5ebe9b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:0cabf8cc197b1f64ecf4bcafcad1ada52c36e0e04bf2dc333a6bd2b1455681e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183283840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d415917245bf606e34fe851d14e7ea9a2056f6f6aa90e52a76712626972ed80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12f7d8d896091b9d2c29a5e6cde8539c46317f69d9bdf7265d00bd18ddc823`  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f0a3b3870a08586645ac30ef5708714e7c9c90f9b6f1b3cacd4be3b20f6f96`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.4 MB (4422742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e47c01863f3d33b323ebe56186312979ef82e360e83db0c91d7cbbecc4d76`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 1.4 MB (1445950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc572deb6e07bab5cfec1a01f207ce6fc2055e184fe1b5fb782af16161dc9756`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7757eda5e7054b021afd94588ac845ca20f9f6bd5b7650f529e0abf767d8bbd7`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 15.3 MB (15296571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56207374222684f02cab68995185ae26d7c5a67bbb67fc6977c8396d5a17cbb3`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd9445023d3822bf6732bb9b9fa3605d1a4690df950c97a017c532b0c05a9c0`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d6ae1e671ec75b33ba508687215f117b0b9bd49f53e12f0b6a640ca1c32c9c`  
		Last Modified: Tue, 24 Dec 2024 22:28:06 GMT  
		Size: 133.9 MB (133876729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71316b0733954834a7be364027252b20eef7e2eedc807a4d947c4becc2283143`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd76318d7ba0eb3de763a6700e0948582a1c1bced04180a47689878d60396e3`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781116e21f02a5a1cd37c34d79b80ea6a295eaf96ae361f077cc3f2fbf0e8372`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ccb5c70138c495bc39acb8e18bf9162a0836057b06b69b4b132149cbdd522e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a03f59a6256eb0460911e70b85e4515be7add82f04c19c8828c74848d9e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7fd24acc577dd92eef36a017f61369c3cb076a0d6a0e173d2fa2aa3820e331b6`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc193d79a49b5a7fbfa30cc9718a3122e18dc8267cdbff710910192de1bc83ea`  
		Last Modified: Tue, 24 Dec 2024 22:28:01 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:6559780c6418602460bd4087f0e0270273ee9fb12a9c7a9291bd71b5ebe9b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0cabf8cc197b1f64ecf4bcafcad1ada52c36e0e04bf2dc333a6bd2b1455681e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183283840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d415917245bf606e34fe851d14e7ea9a2056f6f6aa90e52a76712626972ed80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12f7d8d896091b9d2c29a5e6cde8539c46317f69d9bdf7265d00bd18ddc823`  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f0a3b3870a08586645ac30ef5708714e7c9c90f9b6f1b3cacd4be3b20f6f96`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.4 MB (4422742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e47c01863f3d33b323ebe56186312979ef82e360e83db0c91d7cbbecc4d76`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 1.4 MB (1445950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc572deb6e07bab5cfec1a01f207ce6fc2055e184fe1b5fb782af16161dc9756`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7757eda5e7054b021afd94588ac845ca20f9f6bd5b7650f529e0abf767d8bbd7`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 15.3 MB (15296571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56207374222684f02cab68995185ae26d7c5a67bbb67fc6977c8396d5a17cbb3`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd9445023d3822bf6732bb9b9fa3605d1a4690df950c97a017c532b0c05a9c0`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d6ae1e671ec75b33ba508687215f117b0b9bd49f53e12f0b6a640ca1c32c9c`  
		Last Modified: Tue, 24 Dec 2024 22:28:06 GMT  
		Size: 133.9 MB (133876729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71316b0733954834a7be364027252b20eef7e2eedc807a4d947c4becc2283143`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd76318d7ba0eb3de763a6700e0948582a1c1bced04180a47689878d60396e3`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781116e21f02a5a1cd37c34d79b80ea6a295eaf96ae361f077cc3f2fbf0e8372`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ccb5c70138c495bc39acb8e18bf9162a0836057b06b69b4b132149cbdd522e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a03f59a6256eb0460911e70b85e4515be7add82f04c19c8828c74848d9e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7fd24acc577dd92eef36a017f61369c3cb076a0d6a0e173d2fa2aa3820e331b6`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc193d79a49b5a7fbfa30cc9718a3122e18dc8267cdbff710910192de1bc83ea`  
		Last Modified: Tue, 24 Dec 2024 22:28:01 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:d58ac93387f644e4e040c636b8f50494e78e5afc27ca0a87348b2f577da2b7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ed04aca46b6fe0bdc192becc17d358b46eeb82762b81ee65b80feff3d0873e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170967197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ddbef96911f9f36d1330ffe3f7557c019d49434e738cafabd1a3dd6b4bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746eccf8a0b2af211ab4e965605b2b0650135c559d7afbd8f52b462ace2044b`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d84c48f09d9af270fc8f646b8bbb4527be9af06a10ff2e2d602170036d6f51`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 6.9 MB (6900505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf1ccdd2a47cdbf9c4e42d5ca84f2e3613ee3b362ff84ec757dfad6257f72`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331406986f7012797f213303269b9a4848d879ea3bce49e761b9e0c72e4b5c8`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93598758d10e9e2a9001d29377e0117a3327b7d98dabf670202dc40152aa12c`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 49.6 MB (49616694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c136cb242f20f30b1941cdc2501f981755dae69945f60c417fb3569f5c624b9`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d476cd3429082fc815bde25dc63bfc25061d88441248702ef10a4b05525a`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 64.4 MB (64358700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe60d9fe24a9f2a8a99eeb533a302e7ac771f498e1b28589006b35987e30f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9659be67bd393aa4bf61a8b7c708b4101e9ca8bbcf5ccc4e0aba3b86e166f`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5b82a914b82ea05e740eed150958fe1a7f6d630e32cf2b8dae901f934a8ab7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c8e4cdf3318556f4237a0acd8e65737743e64173f3813bac2a1bd76fa28e8`

```dockerfile
```

-	Layers:
	-	`sha256:a0c4224cdd564e99931920bb22cb968a9924b61182bb9cfbb22c7d4f7c9ce010`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 14.8 MB (14764257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d5c465880406594d1a711f3b62ad657d6852a73721958811351761fa0c1626`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 35.0 KB (34951 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8f440d72abf5fe4b62b257bd2eeafcd44876502e6475b4b9561c35e10fe174f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7cfd1cb86c0741bf55f72560ce6d7799ada94a51f8f192a4d3b689b8496b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683c13940f4ef84a4ff1d4011acef7afdf25ab72317c6eb9b598d99d19fea9`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673fd082ece791ba0f592b131bfdf501d5253fdb4c9dbb8edfa3e0b98f28451`  
		Last Modified: Fri, 22 Nov 2024 05:12:07 GMT  
		Size: 48.5 MB (48487316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6bb492aeb500bcb7145005a8de7a00d65f53abcb65d488ff913809ee5d28e`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928800192ffcde5c4412ef90a10b6e09e646ecca7a2be487c3a73177c99dcc1`  
		Last Modified: Fri, 22 Nov 2024 05:12:08 GMT  
		Size: 71.9 MB (71907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e587e2fcdbcdb874fcb537f5f92bf9e51f032d0df18b282d5bad6f6d83bf3e`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b3ed369b19e67e114654100f91f405ed6c08b1c0b125df65437f5cc0c2152`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8dda4e2465a333987c039420ccd029467a9f0506cf47e2cec741f33c47493753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d4e0f0ac833d92e7a335f89561d45c881a0d9323b2b7ae42aed81e1b60342c`

```dockerfile
```

-	Layers:
	-	`sha256:65a87b45491c89738a6e29c2753f9935e039671e180484a9b85a7a666005f9c7`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 14.8 MB (14759335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6da332c7762246e5423d90bbbee6dcc72800c4471ef8b299f5e79221626dd`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:d58ac93387f644e4e040c636b8f50494e78e5afc27ca0a87348b2f577da2b7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ed04aca46b6fe0bdc192becc17d358b46eeb82762b81ee65b80feff3d0873e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170967197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ddbef96911f9f36d1330ffe3f7557c019d49434e738cafabd1a3dd6b4bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746eccf8a0b2af211ab4e965605b2b0650135c559d7afbd8f52b462ace2044b`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d84c48f09d9af270fc8f646b8bbb4527be9af06a10ff2e2d602170036d6f51`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 6.9 MB (6900505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf1ccdd2a47cdbf9c4e42d5ca84f2e3613ee3b362ff84ec757dfad6257f72`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331406986f7012797f213303269b9a4848d879ea3bce49e761b9e0c72e4b5c8`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93598758d10e9e2a9001d29377e0117a3327b7d98dabf670202dc40152aa12c`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 49.6 MB (49616694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c136cb242f20f30b1941cdc2501f981755dae69945f60c417fb3569f5c624b9`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d476cd3429082fc815bde25dc63bfc25061d88441248702ef10a4b05525a`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 64.4 MB (64358700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe60d9fe24a9f2a8a99eeb533a302e7ac771f498e1b28589006b35987e30f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9659be67bd393aa4bf61a8b7c708b4101e9ca8bbcf5ccc4e0aba3b86e166f`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5b82a914b82ea05e740eed150958fe1a7f6d630e32cf2b8dae901f934a8ab7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c8e4cdf3318556f4237a0acd8e65737743e64173f3813bac2a1bd76fa28e8`

```dockerfile
```

-	Layers:
	-	`sha256:a0c4224cdd564e99931920bb22cb968a9924b61182bb9cfbb22c7d4f7c9ce010`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 14.8 MB (14764257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d5c465880406594d1a711f3b62ad657d6852a73721958811351761fa0c1626`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 35.0 KB (34951 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8f440d72abf5fe4b62b257bd2eeafcd44876502e6475b4b9561c35e10fe174f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7cfd1cb86c0741bf55f72560ce6d7799ada94a51f8f192a4d3b689b8496b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683c13940f4ef84a4ff1d4011acef7afdf25ab72317c6eb9b598d99d19fea9`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673fd082ece791ba0f592b131bfdf501d5253fdb4c9dbb8edfa3e0b98f28451`  
		Last Modified: Fri, 22 Nov 2024 05:12:07 GMT  
		Size: 48.5 MB (48487316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6bb492aeb500bcb7145005a8de7a00d65f53abcb65d488ff913809ee5d28e`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928800192ffcde5c4412ef90a10b6e09e646ecca7a2be487c3a73177c99dcc1`  
		Last Modified: Fri, 22 Nov 2024 05:12:08 GMT  
		Size: 71.9 MB (71907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e587e2fcdbcdb874fcb537f5f92bf9e51f032d0df18b282d5bad6f6d83bf3e`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b3ed369b19e67e114654100f91f405ed6c08b1c0b125df65437f5cc0c2152`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8dda4e2465a333987c039420ccd029467a9f0506cf47e2cec741f33c47493753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d4e0f0ac833d92e7a335f89561d45c881a0d9323b2b7ae42aed81e1b60342c`

```dockerfile
```

-	Layers:
	-	`sha256:65a87b45491c89738a6e29c2753f9935e039671e180484a9b85a7a666005f9c7`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 14.8 MB (14759335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6da332c7762246e5423d90bbbee6dcc72800c4471ef8b299f5e79221626dd`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40`

```console
$ docker pull mysql@sha256:d58ac93387f644e4e040c636b8f50494e78e5afc27ca0a87348b2f577da2b7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40` - linux; amd64

```console
$ docker pull mysql@sha256:ed04aca46b6fe0bdc192becc17d358b46eeb82762b81ee65b80feff3d0873e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170967197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ddbef96911f9f36d1330ffe3f7557c019d49434e738cafabd1a3dd6b4bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746eccf8a0b2af211ab4e965605b2b0650135c559d7afbd8f52b462ace2044b`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d84c48f09d9af270fc8f646b8bbb4527be9af06a10ff2e2d602170036d6f51`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 6.9 MB (6900505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf1ccdd2a47cdbf9c4e42d5ca84f2e3613ee3b362ff84ec757dfad6257f72`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331406986f7012797f213303269b9a4848d879ea3bce49e761b9e0c72e4b5c8`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93598758d10e9e2a9001d29377e0117a3327b7d98dabf670202dc40152aa12c`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 49.6 MB (49616694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c136cb242f20f30b1941cdc2501f981755dae69945f60c417fb3569f5c624b9`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d476cd3429082fc815bde25dc63bfc25061d88441248702ef10a4b05525a`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 64.4 MB (64358700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe60d9fe24a9f2a8a99eeb533a302e7ac771f498e1b28589006b35987e30f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9659be67bd393aa4bf61a8b7c708b4101e9ca8bbcf5ccc4e0aba3b86e166f`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:5b82a914b82ea05e740eed150958fe1a7f6d630e32cf2b8dae901f934a8ab7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c8e4cdf3318556f4237a0acd8e65737743e64173f3813bac2a1bd76fa28e8`

```dockerfile
```

-	Layers:
	-	`sha256:a0c4224cdd564e99931920bb22cb968a9924b61182bb9cfbb22c7d4f7c9ce010`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 14.8 MB (14764257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d5c465880406594d1a711f3b62ad657d6852a73721958811351761fa0c1626`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 35.0 KB (34951 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8f440d72abf5fe4b62b257bd2eeafcd44876502e6475b4b9561c35e10fe174f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7cfd1cb86c0741bf55f72560ce6d7799ada94a51f8f192a4d3b689b8496b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683c13940f4ef84a4ff1d4011acef7afdf25ab72317c6eb9b598d99d19fea9`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673fd082ece791ba0f592b131bfdf501d5253fdb4c9dbb8edfa3e0b98f28451`  
		Last Modified: Fri, 22 Nov 2024 05:12:07 GMT  
		Size: 48.5 MB (48487316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6bb492aeb500bcb7145005a8de7a00d65f53abcb65d488ff913809ee5d28e`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928800192ffcde5c4412ef90a10b6e09e646ecca7a2be487c3a73177c99dcc1`  
		Last Modified: Fri, 22 Nov 2024 05:12:08 GMT  
		Size: 71.9 MB (71907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e587e2fcdbcdb874fcb537f5f92bf9e51f032d0df18b282d5bad6f6d83bf3e`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b3ed369b19e67e114654100f91f405ed6c08b1c0b125df65437f5cc0c2152`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:8dda4e2465a333987c039420ccd029467a9f0506cf47e2cec741f33c47493753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d4e0f0ac833d92e7a335f89561d45c881a0d9323b2b7ae42aed81e1b60342c`

```dockerfile
```

-	Layers:
	-	`sha256:65a87b45491c89738a6e29c2753f9935e039671e180484a9b85a7a666005f9c7`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 14.8 MB (14759335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6da332c7762246e5423d90bbbee6dcc72800c4471ef8b299f5e79221626dd`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-bookworm`

```console
$ docker pull mysql@sha256:6559780c6418602460bd4087f0e0270273ee9fb12a9c7a9291bd71b5ebe9b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:0cabf8cc197b1f64ecf4bcafcad1ada52c36e0e04bf2dc333a6bd2b1455681e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183283840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d415917245bf606e34fe851d14e7ea9a2056f6f6aa90e52a76712626972ed80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12f7d8d896091b9d2c29a5e6cde8539c46317f69d9bdf7265d00bd18ddc823`  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f0a3b3870a08586645ac30ef5708714e7c9c90f9b6f1b3cacd4be3b20f6f96`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.4 MB (4422742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e47c01863f3d33b323ebe56186312979ef82e360e83db0c91d7cbbecc4d76`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 1.4 MB (1445950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc572deb6e07bab5cfec1a01f207ce6fc2055e184fe1b5fb782af16161dc9756`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7757eda5e7054b021afd94588ac845ca20f9f6bd5b7650f529e0abf767d8bbd7`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 15.3 MB (15296571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56207374222684f02cab68995185ae26d7c5a67bbb67fc6977c8396d5a17cbb3`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd9445023d3822bf6732bb9b9fa3605d1a4690df950c97a017c532b0c05a9c0`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d6ae1e671ec75b33ba508687215f117b0b9bd49f53e12f0b6a640ca1c32c9c`  
		Last Modified: Tue, 24 Dec 2024 22:28:06 GMT  
		Size: 133.9 MB (133876729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71316b0733954834a7be364027252b20eef7e2eedc807a4d947c4becc2283143`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd76318d7ba0eb3de763a6700e0948582a1c1bced04180a47689878d60396e3`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781116e21f02a5a1cd37c34d79b80ea6a295eaf96ae361f077cc3f2fbf0e8372`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ccb5c70138c495bc39acb8e18bf9162a0836057b06b69b4b132149cbdd522e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a03f59a6256eb0460911e70b85e4515be7add82f04c19c8828c74848d9e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7fd24acc577dd92eef36a017f61369c3cb076a0d6a0e173d2fa2aa3820e331b6`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc193d79a49b5a7fbfa30cc9718a3122e18dc8267cdbff710910192de1bc83ea`  
		Last Modified: Tue, 24 Dec 2024 22:28:01 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-debian`

```console
$ docker pull mysql@sha256:6559780c6418602460bd4087f0e0270273ee9fb12a9c7a9291bd71b5ebe9b35e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:0cabf8cc197b1f64ecf4bcafcad1ada52c36e0e04bf2dc333a6bd2b1455681e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.3 MB (183283840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d415917245bf606e34fe851d14e7ea9a2056f6f6aa90e52a76712626972ed80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 14 Oct 2024 22:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1debian12
# Mon, 14 Oct 2024 22:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa12f7d8d896091b9d2c29a5e6cde8539c46317f69d9bdf7265d00bd18ddc823`  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f0a3b3870a08586645ac30ef5708714e7c9c90f9b6f1b3cacd4be3b20f6f96`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.4 MB (4422742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54e47c01863f3d33b323ebe56186312979ef82e360e83db0c91d7cbbecc4d76`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 1.4 MB (1445950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc572deb6e07bab5cfec1a01f207ce6fc2055e184fe1b5fb782af16161dc9756`  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7757eda5e7054b021afd94588ac845ca20f9f6bd5b7650f529e0abf767d8bbd7`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 15.3 MB (15296571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56207374222684f02cab68995185ae26d7c5a67bbb67fc6977c8396d5a17cbb3`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd9445023d3822bf6732bb9b9fa3605d1a4690df950c97a017c532b0c05a9c0`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32d6ae1e671ec75b33ba508687215f117b0b9bd49f53e12f0b6a640ca1c32c9c`  
		Last Modified: Tue, 24 Dec 2024 22:28:06 GMT  
		Size: 133.9 MB (133876729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71316b0733954834a7be364027252b20eef7e2eedc807a4d947c4becc2283143`  
		Last Modified: Tue, 24 Dec 2024 22:28:03 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd76318d7ba0eb3de763a6700e0948582a1c1bced04180a47689878d60396e3`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:781116e21f02a5a1cd37c34d79b80ea6a295eaf96ae361f077cc3f2fbf0e8372`  
		Last Modified: Tue, 24 Dec 2024 22:28:04 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ccb5c70138c495bc39acb8e18bf9162a0836057b06b69b4b132149cbdd522e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4028104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310a03f59a6256eb0460911e70b85e4515be7add82f04c19c8828c74848d9e1d`

```dockerfile
```

-	Layers:
	-	`sha256:7fd24acc577dd92eef36a017f61369c3cb076a0d6a0e173d2fa2aa3820e331b6`  
		Last Modified: Tue, 24 Dec 2024 22:28:02 GMT  
		Size: 4.0 MB (3993808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc193d79a49b5a7fbfa30cc9718a3122e18dc8267cdbff710910192de1bc83ea`  
		Last Modified: Tue, 24 Dec 2024 22:28:01 GMT  
		Size: 34.3 KB (34296 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oracle`

```console
$ docker pull mysql@sha256:d58ac93387f644e4e040c636b8f50494e78e5afc27ca0a87348b2f577da2b7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ed04aca46b6fe0bdc192becc17d358b46eeb82762b81ee65b80feff3d0873e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170967197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ddbef96911f9f36d1330ffe3f7557c019d49434e738cafabd1a3dd6b4bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746eccf8a0b2af211ab4e965605b2b0650135c559d7afbd8f52b462ace2044b`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d84c48f09d9af270fc8f646b8bbb4527be9af06a10ff2e2d602170036d6f51`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 6.9 MB (6900505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf1ccdd2a47cdbf9c4e42d5ca84f2e3613ee3b362ff84ec757dfad6257f72`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331406986f7012797f213303269b9a4848d879ea3bce49e761b9e0c72e4b5c8`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93598758d10e9e2a9001d29377e0117a3327b7d98dabf670202dc40152aa12c`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 49.6 MB (49616694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c136cb242f20f30b1941cdc2501f981755dae69945f60c417fb3569f5c624b9`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d476cd3429082fc815bde25dc63bfc25061d88441248702ef10a4b05525a`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 64.4 MB (64358700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe60d9fe24a9f2a8a99eeb533a302e7ac771f498e1b28589006b35987e30f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9659be67bd393aa4bf61a8b7c708b4101e9ca8bbcf5ccc4e0aba3b86e166f`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:5b82a914b82ea05e740eed150958fe1a7f6d630e32cf2b8dae901f934a8ab7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c8e4cdf3318556f4237a0acd8e65737743e64173f3813bac2a1bd76fa28e8`

```dockerfile
```

-	Layers:
	-	`sha256:a0c4224cdd564e99931920bb22cb968a9924b61182bb9cfbb22c7d4f7c9ce010`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 14.8 MB (14764257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d5c465880406594d1a711f3b62ad657d6852a73721958811351761fa0c1626`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 35.0 KB (34951 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8f440d72abf5fe4b62b257bd2eeafcd44876502e6475b4b9561c35e10fe174f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7cfd1cb86c0741bf55f72560ce6d7799ada94a51f8f192a4d3b689b8496b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683c13940f4ef84a4ff1d4011acef7afdf25ab72317c6eb9b598d99d19fea9`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673fd082ece791ba0f592b131bfdf501d5253fdb4c9dbb8edfa3e0b98f28451`  
		Last Modified: Fri, 22 Nov 2024 05:12:07 GMT  
		Size: 48.5 MB (48487316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6bb492aeb500bcb7145005a8de7a00d65f53abcb65d488ff913809ee5d28e`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928800192ffcde5c4412ef90a10b6e09e646ecca7a2be487c3a73177c99dcc1`  
		Last Modified: Fri, 22 Nov 2024 05:12:08 GMT  
		Size: 71.9 MB (71907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e587e2fcdbcdb874fcb537f5f92bf9e51f032d0df18b282d5bad6f6d83bf3e`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b3ed369b19e67e114654100f91f405ed6c08b1c0b125df65437f5cc0c2152`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8dda4e2465a333987c039420ccd029467a9f0506cf47e2cec741f33c47493753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d4e0f0ac833d92e7a335f89561d45c881a0d9323b2b7ae42aed81e1b60342c`

```dockerfile
```

-	Layers:
	-	`sha256:65a87b45491c89738a6e29c2753f9935e039671e180484a9b85a7a666005f9c7`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 14.8 MB (14759335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6da332c7762246e5423d90bbbee6dcc72800c4471ef8b299f5e79221626dd`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oraclelinux9`

```console
$ docker pull mysql@sha256:d58ac93387f644e4e040c636b8f50494e78e5afc27ca0a87348b2f577da2b7ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ed04aca46b6fe0bdc192becc17d358b46eeb82762b81ee65b80feff3d0873e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.0 MB (170967197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c55ddbef96911f9f36d1330ffe3f7557c019d49434e738cafabd1a3dd6b4bac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b746eccf8a0b2af211ab4e965605b2b0650135c559d7afbd8f52b462ace2044b`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d84c48f09d9af270fc8f646b8bbb4527be9af06a10ff2e2d602170036d6f51`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 6.9 MB (6900505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ecf1ccdd2a47cdbf9c4e42d5ca84f2e3613ee3b362ff84ec757dfad6257f72`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6331406986f7012797f213303269b9a4848d879ea3bce49e761b9e0c72e4b5c8`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93598758d10e9e2a9001d29377e0117a3327b7d98dabf670202dc40152aa12c`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 49.6 MB (49616694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c136cb242f20f30b1941cdc2501f981755dae69945f60c417fb3569f5c624b9`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d255d476cd3429082fc815bde25dc63bfc25061d88441248702ef10a4b05525a`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 64.4 MB (64358700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbfe60d9fe24a9f2a8a99eeb533a302e7ac771f498e1b28589006b35987e30f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9659be67bd393aa4bf61a8b7c708b4101e9ca8bbcf5ccc4e0aba3b86e166f`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:5b82a914b82ea05e740eed150958fe1a7f6d630e32cf2b8dae901f934a8ab7e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14799208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8c8e4cdf3318556f4237a0acd8e65737743e64173f3813bac2a1bd76fa28e8`

```dockerfile
```

-	Layers:
	-	`sha256:a0c4224cdd564e99931920bb22cb968a9924b61182bb9cfbb22c7d4f7c9ce010`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 14.8 MB (14764257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98d5c465880406594d1a711f3b62ad657d6852a73721958811351761fa0c1626`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 35.0 KB (34951 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8f440d72abf5fe4b62b257bd2eeafcd44876502e6475b4b9561c35e10fe174f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.5 MB (175482194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e7cfd1cb86c0741bf55f72560ce6d7799ada94a51f8f192a4d3b689b8496b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.40-1.el9
# Mon, 14 Oct 2024 22:15:13 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 14 Oct 2024 22:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e683c13940f4ef84a4ff1d4011acef7afdf25ab72317c6eb9b598d99d19fea9`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b673fd082ece791ba0f592b131bfdf501d5253fdb4c9dbb8edfa3e0b98f28451`  
		Last Modified: Fri, 22 Nov 2024 05:12:07 GMT  
		Size: 48.5 MB (48487316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6bb492aeb500bcb7145005a8de7a00d65f53abcb65d488ff913809ee5d28e`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928800192ffcde5c4412ef90a10b6e09e646ecca7a2be487c3a73177c99dcc1`  
		Last Modified: Fri, 22 Nov 2024 05:12:08 GMT  
		Size: 71.9 MB (71907752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e587e2fcdbcdb874fcb537f5f92bf9e51f032d0df18b282d5bad6f6d83bf3e`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b3ed369b19e67e114654100f91f405ed6c08b1c0b125df65437f5cc0c2152`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8dda4e2465a333987c039420ccd029467a9f0506cf47e2cec741f33c47493753
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14794534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d4e0f0ac833d92e7a335f89561d45c881a0d9323b2b7ae42aed81e1b60342c`

```dockerfile
```

-	Layers:
	-	`sha256:65a87b45491c89738a6e29c2753f9935e039671e180484a9b85a7a666005f9c7`  
		Last Modified: Fri, 22 Nov 2024 05:12:06 GMT  
		Size: 14.8 MB (14759335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be6da332c7762246e5423d90bbbee6dcc72800c4471ef8b299f5e79221626dd`  
		Last Modified: Fri, 22 Nov 2024 05:12:05 GMT  
		Size: 35.2 KB (35199 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oracle`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oraclelinux9`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oracle`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oraclelinux9`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oracle`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:106d5197fd8e4892980469ad42eb20f7a336bd81509aae4ee175d852f5cc4565
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1ecf42d360987627bcf76572ba479f3b5b0a5391a125801617909cc56e7cb22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171508490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3818a28b4a67a9efab3547df8a292de847636d5903f7705d4ccbe1d281b20133`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5cca38a221c35a53694cce3b34887a1cf73335b1c53075114a140a99de0b93`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c84b66ede077e0a8717528112591fbfd5f3ced4040c124eb6659b3c14940d4`  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299f6f88c6cfd0fdcd8f375f1c26bdd1d4f04eded1587b11419b7f8ae0934d3b`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 6.9 MB (6900481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39eae8f992719502e3a1d7552504b1acad7bf67f068af86e0dec581ddad018f`  
		Last Modified: Thu, 21 Nov 2024 23:10:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0557361569a8ecbc29bb910b4bde5cdaad19c06a71ae771a273afa01543d28`  
		Last Modified: Thu, 21 Nov 2024 23:10:57 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d0f80cb1bedb26d1fbd402a1b7788789ef10b76310425c826d463cdcc034e9`  
		Last Modified: Thu, 21 Nov 2024 23:10:59 GMT  
		Size: 47.6 MB (47559709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d496030b710c9fcd2314de6c4b1e7921739e9552cf0338ebd4b51de517252e01`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d755d8c89d19d65a71254593f2410f5bc54a1b5cb51b4763665bbfd08f05451`  
		Last Modified: Thu, 21 Nov 2024 23:11:00 GMT  
		Size: 67.0 MB (66957121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d8e3dc44b682de3b43954ad50435abff0302f59f790cbe032bb70f7edc214`  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:884241880bf669b687d360962b743b33b25533116d683b90f2b94c9ccda0dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14906027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd51641822750b1876ece3ff6912357d7ae33831ceccd80ef88ae8bcb3f8770`

```dockerfile
```

-	Layers:
	-	`sha256:49432bd5eceba50b23ca237ff0a3d2b8faef4b98f24a8d0910671afb2483c998`  
		Last Modified: Thu, 21 Nov 2024 23:10:58 GMT  
		Size: 14.9 MB (14871778 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b5cd99ce99088b40020b732dff8d28f06c94e2d50fa9a1872ba9e33ecb1ec02`  
		Size: 34.2 KB (34249 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:628641565ee2b2f79e9e7904e00bd5a71ec5a68fa6862dc763d8c55a20091ba3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168727861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27efc117602eaf3d70a67093da6305d2a660347a782b49e762997f976116f725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:21:37 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_MAJOR=8.4
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENV MYSQL_SHELL_VERSION=8.4.3-1.el9
# Mon, 14 Oct 2024 22:21:37 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:21:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:21:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:21:37 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:21:37 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbf6d01ca893fbb4c016c7d6b4c0941a4b0a40b3125194eafb7a9a585b62dc7`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f9b21794c38886352090ba8181f07d8a6c3f0a1037da0ea331c1c027e5ec05`  
		Last Modified: Fri, 22 Nov 2024 05:10:36 GMT  
		Size: 46.5 MB (46452190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4b00b72fec9f40e32c595b0d4614bc939895a979f731d49d85db7ad8473db6`  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7a4d749fc90300ad811051e76d69a553d218ef501225fedf92f424e65db05`  
		Last Modified: Fri, 22 Nov 2024 05:10:37 GMT  
		Size: 67.2 MB (67188665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae13e90ab7aa2e5ba35a429ec001df2df298c79d291831dbef6b7571439bee11`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:07512a07387798eea4a8b2e3fafbb3161ed1fe8813142fa5b0cf601bfbc2ba00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14901482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba5ec672d9b424a735a3948ea69d3aaf03ef21ecd0509d563f88f1f89dd9e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:01f4c34afcfe6b37fa777cc16665f3fd1486707bac0736323d642f379958a36b`  
		Last Modified: Fri, 22 Nov 2024 05:10:35 GMT  
		Size: 14.9 MB (14866928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:647eabb9bad75c63cc28c4c33df1dd17da3def588dc639e2e8aad61520108835`  
		Last Modified: Fri, 22 Nov 2024 05:10:34 GMT  
		Size: 34.6 KB (34554 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:0255b469f0135a0236d672d60e3154ae2f4538b146744966d96440318cc822c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:8689c5f93826d949b43a4b7613f9216499694a3082bdc372094a2910082aa391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174293525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56a8c14e14044b8ec7ffb4dd165c8dbe10d4c6ba3d9e754f0c906f52a0b5b4fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5a6a8519b2b1d789b65fe763238531f3456522a13e5e8d6a644ccd9a95e527`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570d30cf82c5e8cd5bde2c25ddc2d5c25e9a38583f09f4411ffce694e1694355`  
		Last Modified: Thu, 21 Nov 2024 23:10:40 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a841bff36f3c6803a0ea0497a2f21ed75fcc7614e9f0fdaf1130861d2052f3f1`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 6.9 MB (6900488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba30c577823a1075c778315bd221b405236429f27ad62b3d359d59e55c640d`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e49e1f26961569a4b36de1ed482bccbb9249ca5b29d0082222bb19d302cca30`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced670fc7f1c77db06886a4b52dc4051543eac07c0f58d481c62f0993e93e365`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 48.2 MB (48213474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9dc7ad7f03decfdeb7260a38115fa61c9d00a8bcaadc00fd9034290cbc8b7f`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d5df9937b5e0d0634c76339346dfac141def2ee29367bf9858ea335714477`  
		Last Modified: Thu, 21 Nov 2024 23:10:44 GMT  
		Size: 69.1 MB (69088378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87d67b89c62ad5e3961e9f730df83c0628049afd874dcfb0df2cd3e7dc5faf`  
		Last Modified: Thu, 21 Nov 2024 23:10:43 GMT  
		Size: 5.3 KB (5324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bfd441919f165324d29d6dd74fd6390229c29c9caaaa05028b5065f915dddc4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14911553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef67873b30995489dff01541aeaca95f24f36e4f8f28a973a8bc988189416c`

```dockerfile
```

-	Layers:
	-	`sha256:743495ad9ec809a83da5647690ff16a19bb1827d608c604db294df594d046bc3`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 14.9 MB (14876237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a27bbc2edf2c9793e06ddecee5fdd4eb5fd0ff2623b658aa7bfad9e16c618dde`  
		Last Modified: Thu, 21 Nov 2024 23:10:42 GMT  
		Size: 35.3 KB (35316 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:493c690c1b115d64b0ad94a41ec4fafff5d799c2811380aaf0a8325fd4ef43d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.5 MB (171501553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50296fefa2a2dbc64120735564ad18b0e51681c58db3b4e5ca17aefad8259c5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:24:51 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["/bin/bash"]
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV GOSU_VERSION=1.17
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_MAJOR=innovation
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENV MYSQL_SHELL_VERSION=9.1.0-1.el9
# Mon, 14 Oct 2024 22:24:51 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
VOLUME [/var/lib/mysql]
# Mon, 14 Oct 2024 22:24:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 14 Oct 2024 22:24:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 14 Oct 2024 22:24:51 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 14 Oct 2024 22:24:51 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbcaadfa83903ddc9308d3aaf06f5d34a9498c7299facf5e699043ad60cfddb3`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0924329359e826029c0b9e3bae69796feef0fffead03a7536e402448e2fb2ab`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595f1ed755a5990b59de61c16bb5578c742a829179eba8151027a643bea940f`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 6.5 MB (6496686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2a5c8574b885b26c607545b32113f35591e98ebfb418f0ef484778ee7bdc2`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15744423bb3522d6ac78de411b79ba1159506a4e4e8ec777b976687c3316dc65`  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51566c62b314a631ab1ce81f65ed731883a011bbb7e7f705b736d46b8c9677eb`  
		Last Modified: Fri, 22 Nov 2024 05:09:00 GMT  
		Size: 47.1 MB (47118691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e9366d891aae4951a873c1f34ce5489903175a32ec09a70cfb0f67027ccd85`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec88e7bec7e8e44e0167c011210730bfc32f47257d04f6151265d105a19ac37`  
		Size: 69.3 MB (69295841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c43ce1f5008e075e34558ca7e05b369bc7b76b9d591b5f2eaeceadbfc601cc`  
		Last Modified: Fri, 22 Nov 2024 05:08:59 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f2b99b6ef6cb4c407ba2f42002153d5f7f5fd8bb7025539fefa6ccc09edfda38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14907079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea58ef4cd8c99d5013748a9b5f638cbef483c4792a480f2f559ef06ae43a70e`

```dockerfile
```

-	Layers:
	-	`sha256:bd8d8fd88bd1a330ae86bb39a0a57e0839a1067fc8b5c76b84ecd37623ad4f34`  
		Last Modified: Fri, 22 Nov 2024 05:08:58 GMT  
		Size: 14.9 MB (14871423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02348e4bd70cad93f1564f16a27f8c334fb881bf6846754de71302d42407208f`  
		Last Modified: Fri, 22 Nov 2024 05:08:57 GMT  
		Size: 35.7 KB (35656 bytes)  
		MIME: application/vnd.in-toto+json
