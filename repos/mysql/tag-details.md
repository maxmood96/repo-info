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
-	[`mysql:8.0.45`](#mysql8045)
-	[`mysql:8.0.45-bookworm`](#mysql8045-bookworm)
-	[`mysql:8.0.45-debian`](#mysql8045-debian)
-	[`mysql:8.0.45-oracle`](#mysql8045-oracle)
-	[`mysql:8.0.45-oraclelinux9`](#mysql8045-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.8`](#mysql848)
-	[`mysql:8.4.8-oracle`](#mysql848-oracle)
-	[`mysql:8.4.8-oraclelinux9`](#mysql848-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.6`](#mysql96)
-	[`mysql:9.6-oracle`](#mysql96-oracle)
-	[`mysql:9.6-oraclelinux9`](#mysql96-oraclelinux9)
-	[`mysql:9.6.0`](#mysql960)
-	[`mysql:9.6.0-oracle`](#mysql960-oracle)
-	[`mysql:9.6.0-oraclelinux9`](#mysql960-oraclelinux9)
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
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:99d774bf02a48a1bb1c599920d2571946d31e5940b854b02737d5e95c184358f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:1681328bca475f89da97cf8b874aa8a6ef3f839bde63e94d65e0f3bb0a62c94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232295488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f5b15e83b660855d14f9ba6bb52e1318f55325be1d3a107e88bff8df9d830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508d7fab5b3b8b90532ffc7564e0fc119bc60af37674722403ca8ca20953958`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442b2c1726efc90cd7c43f9be2775e562529742184ce9ec115a146d18d1a0f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 6.2 MB (6174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9deeee02a57cf31c919d844b5f300212a0ae846a8afdfb7b17ae2d9d18bbd`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbf40285354cf1f5b92fbef7deb3de6bca869fdc714436bd72b55558f534ac`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c1f6f8d5710c5b8128e3e76f9b8af4432cc006169a691d291b8b8693eaf4f`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 49.9 MB (49919614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98f355936672839113a9cc66e9bb5609a34ea5fd65d618bd6b6d992b0668eb`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9003761300d4454af49af00721f47c1aabcf1694af7ffffacb02cf534eae0`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 128.1 MB (128100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a04c019bdea0b50c5201cc75f08d8fbfc60a53da56c2a4a1a78013e6f5df8b`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05db5310ebca836f57d00ce2560dd013c472cdb74dcbc8055c3094d977717c1`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:99aa9dbc770f0d94952937ba365e952bd63760c0c858c55c5171309544783734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64709693d9687e60485a194bf021e3a4d6c3dc1c7ee1da7655c73f3cf295b7f6`

```dockerfile
```

-	Layers:
	-	`sha256:8393005deaacfc65222785d7b6f31410355a8d377ab5b577bed992da27d1e607`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 15.0 MB (14957509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e53730409bb77ba5866bd4832c25876a9dd3d499d6ba6862b55e07066d557a`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f410777cecf10dc5dfd490ffe1489ddcf2cb9052f09927f7363afb2a3b6028b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227907386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c41e46bd2a6334499108b051dde5442107bfb7ef72d3fe63d9b272cf744c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:01 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6452bac61c9846e7a51941a50cb62619f577a6c83a81fd76e35c6333d6148c98`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d97412bc71efc65fe2155a208be247eba6a7bdd7e1ab400e85a91c957f1a37`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b47482305da008b1a5b115c1e06b63ff08a6fb694447e235195c8f1d417b40`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 5.8 MB (5791673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d36ae5423e1e54c5ac34b014de8ece07261e0e2fbbf0044d156b7bd6f2c47`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c576aa7462c33d8a766e00d8877285dcf96dfbc7ea7e93668792cb304ac914`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714c078ee4a4d83291c5ff593e84866ec38f8c0ed269138efc6471205a25922`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 48.8 MB (48779604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d53df0cad0d9a3121fbb4862599c6c65f6de6f2057935c4a736ec0f2316bb0`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0186f5648a58a01455609cbe066414fcca657e5aaead369c5f691e5192e782`  
		Last Modified: Thu, 05 Feb 2026 22:10:34 GMT  
		Size: 126.7 MB (126685581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c56da60d54ffd11d81fbfc1a43d385e517dc9f8310b5a21ef1e82824541406`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0899a5f533cb2a6841804e142e5fde6859a8ef1ed12799a7f888e610799cc`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3ea5d04b7f657e40f86ddf32345aa7d3f13b96a152236708ab73f164efcd43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c833a3def2ca4cc71429ba96a17fee32f693f58a2835ae8f8642a8603b8fd5`

```dockerfile
```

-	Layers:
	-	`sha256:3130a342b3a07253376eec7aba1eb8a76fbe3ef3ded4deb1da5181921f45c40c`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 15.0 MB (14955857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8d836843a88c8e769992602ffc41825b7612d4a5eb946fb72ca2c12ab3189`  
		Last Modified: Thu, 05 Feb 2026 22:10:29 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:99d774bf02a48a1bb1c599920d2571946d31e5940b854b02737d5e95c184358f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1681328bca475f89da97cf8b874aa8a6ef3f839bde63e94d65e0f3bb0a62c94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232295488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f5b15e83b660855d14f9ba6bb52e1318f55325be1d3a107e88bff8df9d830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508d7fab5b3b8b90532ffc7564e0fc119bc60af37674722403ca8ca20953958`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442b2c1726efc90cd7c43f9be2775e562529742184ce9ec115a146d18d1a0f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 6.2 MB (6174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9deeee02a57cf31c919d844b5f300212a0ae846a8afdfb7b17ae2d9d18bbd`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbf40285354cf1f5b92fbef7deb3de6bca869fdc714436bd72b55558f534ac`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c1f6f8d5710c5b8128e3e76f9b8af4432cc006169a691d291b8b8693eaf4f`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 49.9 MB (49919614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98f355936672839113a9cc66e9bb5609a34ea5fd65d618bd6b6d992b0668eb`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9003761300d4454af49af00721f47c1aabcf1694af7ffffacb02cf534eae0`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 128.1 MB (128100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a04c019bdea0b50c5201cc75f08d8fbfc60a53da56c2a4a1a78013e6f5df8b`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05db5310ebca836f57d00ce2560dd013c472cdb74dcbc8055c3094d977717c1`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:99aa9dbc770f0d94952937ba365e952bd63760c0c858c55c5171309544783734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64709693d9687e60485a194bf021e3a4d6c3dc1c7ee1da7655c73f3cf295b7f6`

```dockerfile
```

-	Layers:
	-	`sha256:8393005deaacfc65222785d7b6f31410355a8d377ab5b577bed992da27d1e607`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 15.0 MB (14957509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e53730409bb77ba5866bd4832c25876a9dd3d499d6ba6862b55e07066d557a`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f410777cecf10dc5dfd490ffe1489ddcf2cb9052f09927f7363afb2a3b6028b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227907386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c41e46bd2a6334499108b051dde5442107bfb7ef72d3fe63d9b272cf744c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:01 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6452bac61c9846e7a51941a50cb62619f577a6c83a81fd76e35c6333d6148c98`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d97412bc71efc65fe2155a208be247eba6a7bdd7e1ab400e85a91c957f1a37`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b47482305da008b1a5b115c1e06b63ff08a6fb694447e235195c8f1d417b40`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 5.8 MB (5791673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d36ae5423e1e54c5ac34b014de8ece07261e0e2fbbf0044d156b7bd6f2c47`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c576aa7462c33d8a766e00d8877285dcf96dfbc7ea7e93668792cb304ac914`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714c078ee4a4d83291c5ff593e84866ec38f8c0ed269138efc6471205a25922`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 48.8 MB (48779604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d53df0cad0d9a3121fbb4862599c6c65f6de6f2057935c4a736ec0f2316bb0`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0186f5648a58a01455609cbe066414fcca657e5aaead369c5f691e5192e782`  
		Last Modified: Thu, 05 Feb 2026 22:10:34 GMT  
		Size: 126.7 MB (126685581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c56da60d54ffd11d81fbfc1a43d385e517dc9f8310b5a21ef1e82824541406`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0899a5f533cb2a6841804e142e5fde6859a8ef1ed12799a7f888e610799cc`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3ea5d04b7f657e40f86ddf32345aa7d3f13b96a152236708ab73f164efcd43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c833a3def2ca4cc71429ba96a17fee32f693f58a2835ae8f8642a8603b8fd5`

```dockerfile
```

-	Layers:
	-	`sha256:3130a342b3a07253376eec7aba1eb8a76fbe3ef3ded4deb1da5181921f45c40c`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 15.0 MB (14955857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8d836843a88c8e769992602ffc41825b7612d4a5eb946fb72ca2c12ab3189`  
		Last Modified: Thu, 05 Feb 2026 22:10:29 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:99d774bf02a48a1bb1c599920d2571946d31e5940b854b02737d5e95c184358f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1681328bca475f89da97cf8b874aa8a6ef3f839bde63e94d65e0f3bb0a62c94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232295488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f5b15e83b660855d14f9ba6bb52e1318f55325be1d3a107e88bff8df9d830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508d7fab5b3b8b90532ffc7564e0fc119bc60af37674722403ca8ca20953958`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442b2c1726efc90cd7c43f9be2775e562529742184ce9ec115a146d18d1a0f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 6.2 MB (6174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9deeee02a57cf31c919d844b5f300212a0ae846a8afdfb7b17ae2d9d18bbd`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbf40285354cf1f5b92fbef7deb3de6bca869fdc714436bd72b55558f534ac`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c1f6f8d5710c5b8128e3e76f9b8af4432cc006169a691d291b8b8693eaf4f`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 49.9 MB (49919614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98f355936672839113a9cc66e9bb5609a34ea5fd65d618bd6b6d992b0668eb`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9003761300d4454af49af00721f47c1aabcf1694af7ffffacb02cf534eae0`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 128.1 MB (128100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a04c019bdea0b50c5201cc75f08d8fbfc60a53da56c2a4a1a78013e6f5df8b`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05db5310ebca836f57d00ce2560dd013c472cdb74dcbc8055c3094d977717c1`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:99aa9dbc770f0d94952937ba365e952bd63760c0c858c55c5171309544783734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64709693d9687e60485a194bf021e3a4d6c3dc1c7ee1da7655c73f3cf295b7f6`

```dockerfile
```

-	Layers:
	-	`sha256:8393005deaacfc65222785d7b6f31410355a8d377ab5b577bed992da27d1e607`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 15.0 MB (14957509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e53730409bb77ba5866bd4832c25876a9dd3d499d6ba6862b55e07066d557a`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f410777cecf10dc5dfd490ffe1489ddcf2cb9052f09927f7363afb2a3b6028b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227907386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c41e46bd2a6334499108b051dde5442107bfb7ef72d3fe63d9b272cf744c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:01 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6452bac61c9846e7a51941a50cb62619f577a6c83a81fd76e35c6333d6148c98`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d97412bc71efc65fe2155a208be247eba6a7bdd7e1ab400e85a91c957f1a37`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b47482305da008b1a5b115c1e06b63ff08a6fb694447e235195c8f1d417b40`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 5.8 MB (5791673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d36ae5423e1e54c5ac34b014de8ece07261e0e2fbbf0044d156b7bd6f2c47`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c576aa7462c33d8a766e00d8877285dcf96dfbc7ea7e93668792cb304ac914`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714c078ee4a4d83291c5ff593e84866ec38f8c0ed269138efc6471205a25922`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 48.8 MB (48779604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d53df0cad0d9a3121fbb4862599c6c65f6de6f2057935c4a736ec0f2316bb0`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0186f5648a58a01455609cbe066414fcca657e5aaead369c5f691e5192e782`  
		Last Modified: Thu, 05 Feb 2026 22:10:34 GMT  
		Size: 126.7 MB (126685581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c56da60d54ffd11d81fbfc1a43d385e517dc9f8310b5a21ef1e82824541406`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0899a5f533cb2a6841804e142e5fde6859a8ef1ed12799a7f888e610799cc`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3ea5d04b7f657e40f86ddf32345aa7d3f13b96a152236708ab73f164efcd43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c833a3def2ca4cc71429ba96a17fee32f693f58a2835ae8f8642a8603b8fd5`

```dockerfile
```

-	Layers:
	-	`sha256:3130a342b3a07253376eec7aba1eb8a76fbe3ef3ded4deb1da5181921f45c40c`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 15.0 MB (14955857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8d836843a88c8e769992602ffc41825b7612d4a5eb946fb72ca2c12ab3189`  
		Last Modified: Thu, 05 Feb 2026 22:10:29 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:99d774bf02a48a1bb1c599920d2571946d31e5940b854b02737d5e95c184358f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:1681328bca475f89da97cf8b874aa8a6ef3f839bde63e94d65e0f3bb0a62c94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232295488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f5b15e83b660855d14f9ba6bb52e1318f55325be1d3a107e88bff8df9d830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508d7fab5b3b8b90532ffc7564e0fc119bc60af37674722403ca8ca20953958`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442b2c1726efc90cd7c43f9be2775e562529742184ce9ec115a146d18d1a0f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 6.2 MB (6174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9deeee02a57cf31c919d844b5f300212a0ae846a8afdfb7b17ae2d9d18bbd`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbf40285354cf1f5b92fbef7deb3de6bca869fdc714436bd72b55558f534ac`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c1f6f8d5710c5b8128e3e76f9b8af4432cc006169a691d291b8b8693eaf4f`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 49.9 MB (49919614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98f355936672839113a9cc66e9bb5609a34ea5fd65d618bd6b6d992b0668eb`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9003761300d4454af49af00721f47c1aabcf1694af7ffffacb02cf534eae0`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 128.1 MB (128100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a04c019bdea0b50c5201cc75f08d8fbfc60a53da56c2a4a1a78013e6f5df8b`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05db5310ebca836f57d00ce2560dd013c472cdb74dcbc8055c3094d977717c1`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:99aa9dbc770f0d94952937ba365e952bd63760c0c858c55c5171309544783734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64709693d9687e60485a194bf021e3a4d6c3dc1c7ee1da7655c73f3cf295b7f6`

```dockerfile
```

-	Layers:
	-	`sha256:8393005deaacfc65222785d7b6f31410355a8d377ab5b577bed992da27d1e607`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 15.0 MB (14957509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e53730409bb77ba5866bd4832c25876a9dd3d499d6ba6862b55e07066d557a`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f410777cecf10dc5dfd490ffe1489ddcf2cb9052f09927f7363afb2a3b6028b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227907386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c41e46bd2a6334499108b051dde5442107bfb7ef72d3fe63d9b272cf744c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:01 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6452bac61c9846e7a51941a50cb62619f577a6c83a81fd76e35c6333d6148c98`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d97412bc71efc65fe2155a208be247eba6a7bdd7e1ab400e85a91c957f1a37`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b47482305da008b1a5b115c1e06b63ff08a6fb694447e235195c8f1d417b40`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 5.8 MB (5791673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d36ae5423e1e54c5ac34b014de8ece07261e0e2fbbf0044d156b7bd6f2c47`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c576aa7462c33d8a766e00d8877285dcf96dfbc7ea7e93668792cb304ac914`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714c078ee4a4d83291c5ff593e84866ec38f8c0ed269138efc6471205a25922`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 48.8 MB (48779604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d53df0cad0d9a3121fbb4862599c6c65f6de6f2057935c4a736ec0f2316bb0`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0186f5648a58a01455609cbe066414fcca657e5aaead369c5f691e5192e782`  
		Last Modified: Thu, 05 Feb 2026 22:10:34 GMT  
		Size: 126.7 MB (126685581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c56da60d54ffd11d81fbfc1a43d385e517dc9f8310b5a21ef1e82824541406`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0899a5f533cb2a6841804e142e5fde6859a8ef1ed12799a7f888e610799cc`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:3ea5d04b7f657e40f86ddf32345aa7d3f13b96a152236708ab73f164efcd43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c833a3def2ca4cc71429ba96a17fee32f693f58a2835ae8f8642a8603b8fd5`

```dockerfile
```

-	Layers:
	-	`sha256:3130a342b3a07253376eec7aba1eb8a76fbe3ef3ded4deb1da5181921f45c40c`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 15.0 MB (14955857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8d836843a88c8e769992602ffc41825b7612d4a5eb946fb72ca2c12ab3189`  
		Last Modified: Thu, 05 Feb 2026 22:10:29 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:7acd9677ba9d3d1c91a3b2a7999e182ca15919c5f2577184e5c8ce5384867ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:c88b2966f8d78d6c472db6377763197fc5774a8ba97ec9f57a6ff0d3fe772f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183455196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c4a4fc4c92e2f74ad4b520e0ac1c0cd04657daf98d4fb19284faeb4a18c30d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:46:25 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 03 Feb 2026 02:46:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
ENV GOSU_VERSION=1.19
# Tue, 03 Feb 2026 02:46:37 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 03 Feb 2026 02:46:37 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 03 Feb 2026 02:46:41 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Tue, 03 Feb 2026 02:46:41 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 03 Feb 2026 02:46:51 GMT
VOLUME [/var/lib/mysql]
# Tue, 03 Feb 2026 02:46:52 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 03 Feb 2026 02:46:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Feb 2026 02:46:52 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 03 Feb 2026 02:46:52 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a5b80be3d206e2d435eb2fc79c4623971beadba45794ef9deef75056678f2`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2807f6690bf06bbc986ce9606ba63efd99f66abbae9798fd0167f88fbb5e5791`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.4 MB (4423358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390364b7cb489b84f87c7dd04bdcd1048a48f58c4fd6ff6d9ea72da1a6e6d5c0`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 1.2 MB (1248707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9554903e7736c5d8f7b7f55e7415eabf2405cd446a43edfddafa7c6286e63ce0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:354b42ea21251d1c75495137c0b130e80dc2ac8489f5e3adcba1e286544e77aa`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 15.3 MB (15295785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c60a419dab667eb8827182fc05853bacf0ce5e7ff087351c5c751f5e6eb37`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 3.1 KB (3051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c89033c9288c84853dd0a6d71cdc415bc831a3656ba668a3aa81362e62aad8`  
		Last Modified: Tue, 03 Feb 2026 02:47:16 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063b17299955d859a8e1b32e0f3952b7b57cf1f5ad9373d0903c004149df4148`  
		Last Modified: Tue, 03 Feb 2026 02:47:19 GMT  
		Size: 134.2 MB (134248036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dceb9e5c858383d3d0b5ba1491438d474c06295976d6e2f3c83eeb9a0122ce`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2869138c6b4ff8241e2db2830f9d3b9a66ebe77131a646d714e8b18f320d0987`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6989dcf05dba38919967de86430479b2f335e797d02a5544b4e762e7ab2b1ec0`  
		Last Modified: Tue, 03 Feb 2026 02:47:17 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:dbe0a4479f233139b9eb8adf0b03e92d919122372f0f7ad39f07d119b742fbce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8538e8c059b5ca915a6dc989d5fb514583745c1c16448916277e840ecaed9ad0`

```dockerfile
```

-	Layers:
	-	`sha256:6d0101433645a391a811908465f7e49b435d4e5a614d863eff639c10681ea4d0`  
		Last Modified: Tue, 03 Feb 2026 02:47:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a9ba8961725ea31918907f32cbd844efb69d2d6f0a4f4bfae0c43c9973f6730`  
		Last Modified: Tue, 03 Feb 2026 02:47:14 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:99d774bf02a48a1bb1c599920d2571946d31e5940b854b02737d5e95c184358f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1681328bca475f89da97cf8b874aa8a6ef3f839bde63e94d65e0f3bb0a62c94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232295488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f5b15e83b660855d14f9ba6bb52e1318f55325be1d3a107e88bff8df9d830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508d7fab5b3b8b90532ffc7564e0fc119bc60af37674722403ca8ca20953958`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442b2c1726efc90cd7c43f9be2775e562529742184ce9ec115a146d18d1a0f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 6.2 MB (6174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9deeee02a57cf31c919d844b5f300212a0ae846a8afdfb7b17ae2d9d18bbd`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbf40285354cf1f5b92fbef7deb3de6bca869fdc714436bd72b55558f534ac`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c1f6f8d5710c5b8128e3e76f9b8af4432cc006169a691d291b8b8693eaf4f`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 49.9 MB (49919614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98f355936672839113a9cc66e9bb5609a34ea5fd65d618bd6b6d992b0668eb`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9003761300d4454af49af00721f47c1aabcf1694af7ffffacb02cf534eae0`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 128.1 MB (128100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a04c019bdea0b50c5201cc75f08d8fbfc60a53da56c2a4a1a78013e6f5df8b`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05db5310ebca836f57d00ce2560dd013c472cdb74dcbc8055c3094d977717c1`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:99aa9dbc770f0d94952937ba365e952bd63760c0c858c55c5171309544783734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64709693d9687e60485a194bf021e3a4d6c3dc1c7ee1da7655c73f3cf295b7f6`

```dockerfile
```

-	Layers:
	-	`sha256:8393005deaacfc65222785d7b6f31410355a8d377ab5b577bed992da27d1e607`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 15.0 MB (14957509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e53730409bb77ba5866bd4832c25876a9dd3d499d6ba6862b55e07066d557a`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f410777cecf10dc5dfd490ffe1489ddcf2cb9052f09927f7363afb2a3b6028b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227907386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c41e46bd2a6334499108b051dde5442107bfb7ef72d3fe63d9b272cf744c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:01 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6452bac61c9846e7a51941a50cb62619f577a6c83a81fd76e35c6333d6148c98`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d97412bc71efc65fe2155a208be247eba6a7bdd7e1ab400e85a91c957f1a37`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b47482305da008b1a5b115c1e06b63ff08a6fb694447e235195c8f1d417b40`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 5.8 MB (5791673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d36ae5423e1e54c5ac34b014de8ece07261e0e2fbbf0044d156b7bd6f2c47`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c576aa7462c33d8a766e00d8877285dcf96dfbc7ea7e93668792cb304ac914`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714c078ee4a4d83291c5ff593e84866ec38f8c0ed269138efc6471205a25922`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 48.8 MB (48779604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d53df0cad0d9a3121fbb4862599c6c65f6de6f2057935c4a736ec0f2316bb0`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0186f5648a58a01455609cbe066414fcca657e5aaead369c5f691e5192e782`  
		Last Modified: Thu, 05 Feb 2026 22:10:34 GMT  
		Size: 126.7 MB (126685581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c56da60d54ffd11d81fbfc1a43d385e517dc9f8310b5a21ef1e82824541406`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0899a5f533cb2a6841804e142e5fde6859a8ef1ed12799a7f888e610799cc`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3ea5d04b7f657e40f86ddf32345aa7d3f13b96a152236708ab73f164efcd43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c833a3def2ca4cc71429ba96a17fee32f693f58a2835ae8f8642a8603b8fd5`

```dockerfile
```

-	Layers:
	-	`sha256:3130a342b3a07253376eec7aba1eb8a76fbe3ef3ded4deb1da5181921f45c40c`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 15.0 MB (14955857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8d836843a88c8e769992602ffc41825b7612d4a5eb946fb72ca2c12ab3189`  
		Last Modified: Thu, 05 Feb 2026 22:10:29 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:99d774bf02a48a1bb1c599920d2571946d31e5940b854b02737d5e95c184358f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1681328bca475f89da97cf8b874aa8a6ef3f839bde63e94d65e0f3bb0a62c94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232295488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272f5b15e83b660855d14f9ba6bb52e1318f55325be1d3a107e88bff8df9d830`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:27 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:49 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:49 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f508d7fab5b3b8b90532ffc7564e0fc119bc60af37674722403ca8ca20953958`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d442b2c1726efc90cd7c43f9be2775e562529742184ce9ec115a146d18d1a0f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 6.2 MB (6174571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a9deeee02a57cf31c919d844b5f300212a0ae846a8afdfb7b17ae2d9d18bbd`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fbf40285354cf1f5b92fbef7deb3de6bca869fdc714436bd72b55558f534ac`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2c1f6f8d5710c5b8128e3e76f9b8af4432cc006169a691d291b8b8693eaf4f`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 49.9 MB (49919614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce98f355936672839113a9cc66e9bb5609a34ea5fd65d618bd6b6d992b0668eb`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae9003761300d4454af49af00721f47c1aabcf1694af7ffffacb02cf534eae0`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 128.1 MB (128100613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a04c019bdea0b50c5201cc75f08d8fbfc60a53da56c2a4a1a78013e6f5df8b`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05db5310ebca836f57d00ce2560dd013c472cdb74dcbc8055c3094d977717c1`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:99aa9dbc770f0d94952937ba365e952bd63760c0c858c55c5171309544783734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64709693d9687e60485a194bf021e3a4d6c3dc1c7ee1da7655c73f3cf295b7f6`

```dockerfile
```

-	Layers:
	-	`sha256:8393005deaacfc65222785d7b6f31410355a8d377ab5b577bed992da27d1e607`  
		Last Modified: Thu, 05 Feb 2026 22:10:12 GMT  
		Size: 15.0 MB (14957509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6e53730409bb77ba5866bd4832c25876a9dd3d499d6ba6862b55e07066d557a`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:f410777cecf10dc5dfd490ffe1489ddcf2cb9052f09927f7363afb2a3b6028b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227907386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843c41e46bd2a6334499108b051dde5442107bfb7ef72d3fe63d9b272cf744c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:27 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:29 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:29 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 05 Feb 2026 22:08:56 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:08:56 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:25 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 05 Feb 2026 22:10:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:01 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:01 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6452bac61c9846e7a51941a50cb62619f577a6c83a81fd76e35c6333d6148c98`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d97412bc71efc65fe2155a208be247eba6a7bdd7e1ab400e85a91c957f1a37`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b47482305da008b1a5b115c1e06b63ff08a6fb694447e235195c8f1d417b40`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 5.8 MB (5791673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042d36ae5423e1e54c5ac34b014de8ece07261e0e2fbbf0044d156b7bd6f2c47`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c576aa7462c33d8a766e00d8877285dcf96dfbc7ea7e93668792cb304ac914`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714c078ee4a4d83291c5ff593e84866ec38f8c0ed269138efc6471205a25922`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 48.8 MB (48779604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d53df0cad0d9a3121fbb4862599c6c65f6de6f2057935c4a736ec0f2316bb0`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0186f5648a58a01455609cbe066414fcca657e5aaead369c5f691e5192e782`  
		Last Modified: Thu, 05 Feb 2026 22:10:34 GMT  
		Size: 126.7 MB (126685581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c56da60d54ffd11d81fbfc1a43d385e517dc9f8310b5a21ef1e82824541406`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e0899a5f533cb2a6841804e142e5fde6859a8ef1ed12799a7f888e610799cc`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3ea5d04b7f657e40f86ddf32345aa7d3f13b96a152236708ab73f164efcd43ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c833a3def2ca4cc71429ba96a17fee32f693f58a2835ae8f8642a8603b8fd5`

```dockerfile
```

-	Layers:
	-	`sha256:3130a342b3a07253376eec7aba1eb8a76fbe3ef3ded4deb1da5181921f45c40c`  
		Last Modified: Thu, 05 Feb 2026 22:10:30 GMT  
		Size: 15.0 MB (14955857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cc8d836843a88c8e769992602ffc41825b7612d4a5eb946fb72ca2c12ab3189`  
		Last Modified: Thu, 05 Feb 2026 22:10:29 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:7fcf7bcd3fa703ff23a2b998e4ed9077e5db570bcc4468459902e33b23d2841d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:683eb124e222ffca894ba53f35c84bfd43e3e6343664ca909c09a8a45aeffc23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233220071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c562866f17cc749b3082dc8a1602ea707a134145679f048a3c0f41c9e36713a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:23 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:25 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:47 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:48 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:48 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:13 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3202636d61f308e37499c87644535b315fa6d989c7fdbf9140ef480ff570d07`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccfd188136ea5c39fd741aaa68c04a1312bca49803a517c8a1ff4e9ae94832a`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9455481d2b938256b11b624ecd8eab2fbf002c132d14c95fa19b6315066d5b`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 6.2 MB (6174550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75882d54c3d8839f01970b3adb9e3d007ff23bd64437aefaceea6e2294ead050`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2e50d8b4d194b488b0a9645af73c0fb4927d433780a589b7d06c86e9ef9a07`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb84af18ccbf7a3575f64e23770f09e23be35fec89d896e42e4f5c3154ef765`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 47.8 MB (47809670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7fb090b90f53c38ba9bb2b1b0f3f56f9e2b620fc4bf72d55b4f906481d8d53`  
		Last Modified: Thu, 05 Feb 2026 22:10:14 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2c353aa8db811ce8bcbd9414dc87c177fa42b8d326e951f981bd47ec0c1e48`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 131.1 MB (131135274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952b63b654ecc06674b303b2e2886751b6cd7266e41b6306bb769109bd9e8e44`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7a74da631d30d673b08445ea567ab2a527f339481b81da9c2fc404f59fc1ca35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401659ea4fd8365e01cf6b968d18121cb64768b7e9a2cffdb83ec54b69ae1315`

```dockerfile
```

-	Layers:
	-	`sha256:a8ffb24fde156b685027105f2e49e41de46ed71f5acbd64bfb8f9c185f03f2da`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 15.2 MB (15234330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ab5109edccef37f621463e5fe340894bfeb106b83509cd4fab0f9c216de3d7`  
		Last Modified: Thu, 05 Feb 2026 22:10:13 GMT  
		Size: 34.2 KB (34208 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:887b42d136c770e6765d5734afff08ca9bfeebf1ab0c50e0e8965fbd98961d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228690481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e8c34d2aea36d58feff2312af7dee562782d1e7ea06aa95f26f52454e8b5f98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:25 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:28 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:28 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:54 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_MAJOR=8.4
# Thu, 05 Feb 2026 22:08:55 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:08:55 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Thu, 05 Feb 2026 22:10:00 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:00 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde62e757594d7dc6c599378f48c11df87a1d86cc44d8dab32436c399ca12c69`  
		Last Modified: Thu, 05 Feb 2026 22:10:11 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c2b04bb0279edea32f0b6a879d9972e498f605db208acf90303d7edef08b9f`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 737.5 KB (737528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6596c755be37d688c5ab682fb623d26dadcdb449be734808207123a7e6b757`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 5.8 MB (5791664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d35ace2720d0312b242a590f8800362e2d384365d5ff9c4549d7e9b365cd7d`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f5d698bd2df1cffa04b24cde9f83112f0cb6df57764d36152995e7c9fa1a0b`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15dcdf3c901e95b0cef2eb033c62bad46051856edd1535b0b25bed43208700fd`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 46.7 MB (46700639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee0fb34aa4b77061e4ae704b512f04def99f120cb362a171700d4c121b7e42d`  
		Last Modified: Thu, 05 Feb 2026 22:10:32 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7424f8225a8a1da0d034b00cef584bfe12de313a0e3e6979281e58d727a5d78`  
		Last Modified: Thu, 05 Feb 2026 22:10:36 GMT  
		Size: 129.5 MB (129547767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2f27d2d8bf8d08127bcc327a9cb5d75fcf2468eeb6a1dcd15db9b7e5de448c8`  
		Last Modified: Thu, 05 Feb 2026 22:10:33 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fdcf2bb0bd1f366e5df38239c78be35033593c813f5646e21edaafbda4899e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec514cde294031c95a24697c022b26c5c5f1dfde6377de4816e22b508973f7a`

```dockerfile
```

-	Layers:
	-	`sha256:ab3fc442e6d7d7420ff4f2c2395ab29c102a7873a60c701d8b8bd58e408126a5`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 15.2 MB (15232750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9d144448f5e2a19c678d6b575576b636f5606518f88fe56a449ebe4ad6be78`  
		Last Modified: Thu, 05 Feb 2026 22:10:31 GMT  
		Size: 34.5 KB (34513 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:db32c8ec843c042a728efb0ac7aa814d6f010eaac8923e20ae0a849d09c5baf8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:717d1e4b2352def1f05b40c3c16c470b57f320112a32e506d4548f9964853304
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66b7a28811314e6a4dcafccd94c4be68006bc32ec970bf95deb46ba36faaaca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:02:11 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:02:11 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:16 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:19 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:19 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:41 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:42 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:42 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:09:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:09:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:09:44 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:09:44 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:4f37333d1be658a226cdafd622c7bda0a95abbcb999c29a571136add51950044`  
		Last Modified: Thu, 05 Feb 2026 22:02:22 GMT  
		Size: 47.3 MB (47307542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a384f12fc17c4a4345d1165feb19288c5437373be4ac09f162d08c68683b26`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3034072b44e63d1e79ea3e342fd12e97ca43901fd8b2906e210eae290c723f`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 783.6 KB (783559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07617e6f14bd1f717d9551f5b325d7412b1ca9fe16f6130958b1911d5bc5ec2`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 6.2 MB (6174544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e7dc27e1ddd2f888a1d6ad0cad0c55905bb5b2276a717cca00b0e9b4deb667`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1ba0190807d166baef7098e86fe6204c122fae6772a54f1f35fc9d174c61e`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c2157be11ce559af0bc6b6d25eb94ef104993abedc0584fc94d62731fd5311`  
		Last Modified: Thu, 05 Feb 2026 22:10:19 GMT  
		Size: 51.4 MB (51448952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e9390a44189a01556582762353a051263135785885eb2e15147586d679667a`  
		Last Modified: Thu, 05 Feb 2026 22:10:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b95dea655397746f06b33bf365db15297f55c2345090a2823bc0c79874b9a4`  
		Last Modified: Thu, 05 Feb 2026 22:10:21 GMT  
		Size: 160.6 MB (160633758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe44c8bf49c1d239b0eda62ea1c5ed07cc67057612dcca8831df4b67a83cc1f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:18 GMT  
		Size: 5.3 KB (5332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d28c84384e7ddf32b134e617d8e0822e7f6d7095cc30579de46a1ee9d2768ba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e177d6dc600e09c21080e1102e8a416e021c4a0525695f8053429294cf92caf2`

```dockerfile
```

-	Layers:
	-	`sha256:7e5a775ad22a51cb9a2257f84e44d71f2a18eb24914dc233ce465adf051f25c4`  
		Last Modified: Thu, 05 Feb 2026 22:10:16 GMT  
		Size: 16.3 MB (16297420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc8be4b9c0eb42b0ba27f1212994a66b32c067b642fe4e9d0954f857a6ca0812`  
		Last Modified: Thu, 05 Feb 2026 22:10:15 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:8da8ea39f953a1dc0a507576ba3289a6416caa5a195ecdeefb5ad34991fc648b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01bab0412e25056497796fd66a0e8a8ba88fd150ae0215a902ac40aec72e33b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 05 Feb 2026 22:01:48 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 05 Feb 2026 22:01:48 GMT
CMD ["/bin/bash"]
# Thu, 05 Feb 2026 22:08:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 05 Feb 2026 22:08:26 GMT
ENV GOSU_VERSION=1.19
# Thu, 05 Feb 2026 22:08:26 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 05 Feb 2026 22:08:52 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 05 Feb 2026 22:08:53 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:08:53 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 05 Feb 2026 22:09:22 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Thu, 05 Feb 2026 22:10:04 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
VOLUME [/var/lib/mysql]
# Thu, 05 Feb 2026 22:10:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 05 Feb 2026 22:10:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Feb 2026 22:10:04 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 05 Feb 2026 22:10:04 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:bdaccdb6a2d14a7ee18a3d1ff57e3f6bd4e826bf7bda3d4995e73942beb6ca3a`  
		Last Modified: Thu, 05 Feb 2026 22:02:00 GMT  
		Size: 45.9 MB (45903410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc311b7141a81abc777678fce031f5f9d0e35f00fac0bc09149d034df7fb143`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2866f080bd66e1591ef99259b84bfce1897c9a1cc90704bbef47668c2cc91263`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 737.5 KB (737524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9e9c3d0312fcc60a59444875726e7498141d132a2a5b691f8d010c93eb500a`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 5.8 MB (5791701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3308f5dc5a765736e142932bff2e7f514adacbf784323b1281d3bc75406f328`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bd823d80b302358df95e02d0ff68bd90af04955af6d39800c87ffffafef16f5`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c8f56b46ceb0491f6906a0dd4f6bf82d59a73f9a023c7e00ee74741b84d70f`  
		Last Modified: Thu, 05 Feb 2026 22:10:42 GMT  
		Size: 50.1 MB (50086840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74b2b2e44e46310cc4b14e96034786d2aed014890bd99635ae0178641075038`  
		Last Modified: Thu, 05 Feb 2026 22:10:40 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e577a10e09c5ae91c9924eae74caedacee1690b00ff2fc22bcfd550113218`  
		Last Modified: Thu, 05 Feb 2026 22:10:44 GMT  
		Size: 158.9 MB (158940066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad37a81ec0b0df85dfc6fa4d746388caf1533f0bfb64ee04f1c32601eabcb9ef`  
		Last Modified: Thu, 05 Feb 2026 22:10:41 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f65d1491a46324caebad462221004ac9e42e2a377e2c601ea502389b47e05a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992b8c30aee19df4cb17ae696682f32b0923a3eec31a06d8d8bde4992f250b27`

```dockerfile
```

-	Layers:
	-	`sha256:381b00c5f847ba4f949cafdcc0911c4eaf169d35cdf464ac47ef92670595b931`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 16.3 MB (16295876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c08a75f7468a7ab9c1aec376a6792433ca750a3fb5f6f80345a2bbe861919f1`  
		Last Modified: Thu, 05 Feb 2026 22:10:39 GMT  
		Size: 35.6 KB (35616 bytes)  
		MIME: application/vnd.in-toto+json
