<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:8`](#mysql8)
-	[`mysql:8-oracle`](#mysql8-oracle)
-	[`mysql:8-oraclelinux8`](#mysql8-oraclelinux8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0-bookworm`](#mysql80-bookworm)
-	[`mysql:8.0-debian`](#mysql80-debian)
-	[`mysql:8.0-oracle`](#mysql80-oracle)
-	[`mysql:8.0-oraclelinux8`](#mysql80-oraclelinux8)
-	[`mysql:8.0.36`](#mysql8036)
-	[`mysql:8.0.36-bookworm`](#mysql8036-bookworm)
-	[`mysql:8.0.36-debian`](#mysql8036-debian)
-	[`mysql:8.0.36-oracle`](#mysql8036-oracle)
-	[`mysql:8.0.36-oraclelinux8`](#mysql8036-oraclelinux8)
-	[`mysql:8.3`](#mysql83)
-	[`mysql:8.3-oracle`](#mysql83-oracle)
-	[`mysql:8.3-oraclelinux8`](#mysql83-oraclelinux8)
-	[`mysql:8.3.0`](#mysql830)
-	[`mysql:8.3.0-oracle`](#mysql830-oracle)
-	[`mysql:8.3.0-oraclelinux8`](#mysql830-oraclelinux8)
-	[`mysql:innovation`](#mysqlinnovation)
-	[`mysql:innovation-oracle`](#mysqlinnovation-oracle)
-	[`mysql:innovation-oraclelinux8`](#mysqlinnovation-oraclelinux8)
-	[`mysql:latest`](#mysqllatest)
-	[`mysql:oracle`](#mysqloracle)
-	[`mysql:oraclelinux8`](#mysqloraclelinux8)

## `mysql:8`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux8`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:92923e99278839ae86ba3edde972cf46f620ada05b37f85db04398cf8d7fc2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:9aa790f95200ad044e57741ad3b23ef8b396d4be7ae85b4b8696c9bbc7168b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174790853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f309f7dabfd1bb9a6f8ce65028d1fc1636074e4463676580894e5b59af10c4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09b1c7d50d0745c852e3f217b873c881e4573e8d482fdf12e07cae62461b97`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a6697daf1314aef2e087deadaa18e37fee5b2d1044569bf7c4ee700e5d123`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f40b0c53d71d13804fba188a21df731aa9ada6cf0ba757ef1638030ed7039c`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 4.6 MB (4607397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fdbb420ffeea98a18e309057fbb3b3a93157947eb7a9b610e02ccf0b88b9a`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964da5c649e204b4fb39c391ee0a9cdaa0e99dda9bbb4710a4d6cf86e1d673dd`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd68fed930245b826c61227ba6656e8f67463016b85c66ef658bcf057119744`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 58.5 MB (58529828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f88f90d943bbaf7143ec068d33df13c22e37019667234fee196dd3bc72b3d3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9e6ae336c3aa275cccadc6f2fa6df826424c19d8ddb96f320866b0e5788c3`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 59.3 MB (59333952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3624bb597fc3508d4c21b075ad07b46c2252da9a92a1235093b343dbf6a421`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5c5a90ca7f47acc73cc8db3d9e47a4a6a55a29f57e42820f8ec78fe7598ed`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:570f9b1f56a0f792e296d72a362dcc0874e29d11fe6d251d354a1ea5c5c6b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de4182006b637eafd896bc623ec2b30695e0cf68ea9169df4021da1b47672b`

```dockerfile
```

-	Layers:
	-	`sha256:f742d61ef088a638e7c67a6585099be1b7987149874f9b2b7f7d4ac4cbd44da8`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 14.2 MB (14248912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2bd61f95a481fb980f77c2b1474b462a544dfa1f4c8d16eb3dd89b9f78ded8`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26df16d3c97cc9142b77402aa8d29418e98b073dc3a692738f0a5ae3e647d90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178451913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73c6e55254408fd327a42eefb5477d001c395b6a9a260379c96b645db52301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf5f8b6640146cdb4a35578f6a3e8f4e8b48f03c870f8187c4c79909771378`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdeddc397e162f8ca0732bbb6c994ecd3098d6fdc2b37691acf4f07f6ade95`  
		Last Modified: Wed, 14 Feb 2024 11:02:27 GMT  
		Size: 57.6 MB (57579757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51065c28a837882374674779bc906cd6f6350b15ca440863c760b60885aaa93e`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bd88fdeb3df2956cdbdca413b27546d8cdece2d0a4656e3c0d31a0efa255f`  
		Last Modified: Wed, 14 Feb 2024 11:02:26 GMT  
		Size: 65.6 MB (65580430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242e8cb8356c83f92af998acbf475f04ca5794948510d561d5d4405c396b184`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2629cfe75be9f6fda271ec2ab14026f96f570f8b3a4ac0c669669a9e94bfc`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:71bd429485fbd27de87bc6df70171585bab325ba725fe33f41638d2a28e5c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64716502b2bee010019f103bd457ed7c4d2c0c8a79ab2e1cf9d002f745509324`

```dockerfile
```

-	Layers:
	-	`sha256:80ae47d0d6b69d63962cc882f027a0d561c20514fbea063ba66f16374725564b`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be015ae2a767b85f837175108bc9c2e71cf8e05064cc9e68e5c58c02e6cda6a`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:b64e2d58cc179e38acb0ccdae5a5a91368f93a00fef422ed34cf6a698e1c0d32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:cfb4769acf1cd2945a83f401810a12883a905d148b6f01f8b739d46809b5af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180826047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e09efbec746077116fffe18e56f6af97f369d8aec7868226048248ca2fff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 21:25:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV GOSU_VERSION=1.16
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Wed, 28 Feb 2024 21:25:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Feb 2024 21:25:11 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 21:25:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Feb 2024 21:25:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93500000d2237d1a816fbad4d4d96c74914a325c087554b804c977d52b12d0`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca73a9485b2e290356558877f1aac55608843603177fe71830317451c0c38eb6`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.4 MB (4422794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc655ca6ff77811573539289d01ffdf3f02b46002efb715aab3391cbb9a0689`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.4 MB (1445462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099440dd6678c36a1c79ea9f8af24dcfb826128159dee2273f9ccb7fbee184f9`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d32c3d97d54b2b2994d7f203c7d31276afeb633bf49a3a923f7d6f2abc8b2`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 15.3 MB (15281620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038b55db03e70b5044da4ab6e7a0b4b2839d81f119499eadc2530d46f50f68f5`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e3b64441767050d3e4ef7303a90b1b1f8316cd576f5c03849ba4df0622b4cc`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3fd9fe1c53d7035167e80161764c3f1f32ea0f8e848d05b8b195ea7cadc024`  
		Last Modified: Thu, 29 Feb 2024 19:49:55 GMT  
		Size: 130.5 MB (130541962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d966ddd4cb66db76e594361804b9af9f464d131615c6d831680ad93160d93396`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e4e71c2dd1e003a55d7d71bb9605962da10a0fe01ab4389c7ed73d3554004`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96448d3612a0568a7546321726cc4614b4660669dbcb013d84927f3e5d46044c`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ac485df781b5855a726f9a564247f671b05307b9a60d7edc47fe5fa4ddd59179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4fb44125c8deb9411165816461a05957a0ba9fdb1392107b8189bc4c8a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:5eed377ab5863f68540f4fdf25e5f6115c22cea7a09d6fd2a5f397fe71cbc0ac`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.0 MB (3954775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21933d6ce644b261242766852efeea75729d4372bd091955a5bd3f41798b2ed6`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:b64e2d58cc179e38acb0ccdae5a5a91368f93a00fef422ed34cf6a698e1c0d32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cfb4769acf1cd2945a83f401810a12883a905d148b6f01f8b739d46809b5af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180826047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e09efbec746077116fffe18e56f6af97f369d8aec7868226048248ca2fff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 21:25:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV GOSU_VERSION=1.16
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Wed, 28 Feb 2024 21:25:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Feb 2024 21:25:11 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 21:25:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Feb 2024 21:25:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93500000d2237d1a816fbad4d4d96c74914a325c087554b804c977d52b12d0`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca73a9485b2e290356558877f1aac55608843603177fe71830317451c0c38eb6`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.4 MB (4422794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc655ca6ff77811573539289d01ffdf3f02b46002efb715aab3391cbb9a0689`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.4 MB (1445462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099440dd6678c36a1c79ea9f8af24dcfb826128159dee2273f9ccb7fbee184f9`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d32c3d97d54b2b2994d7f203c7d31276afeb633bf49a3a923f7d6f2abc8b2`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 15.3 MB (15281620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038b55db03e70b5044da4ab6e7a0b4b2839d81f119499eadc2530d46f50f68f5`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e3b64441767050d3e4ef7303a90b1b1f8316cd576f5c03849ba4df0622b4cc`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3fd9fe1c53d7035167e80161764c3f1f32ea0f8e848d05b8b195ea7cadc024`  
		Last Modified: Thu, 29 Feb 2024 19:49:55 GMT  
		Size: 130.5 MB (130541962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d966ddd4cb66db76e594361804b9af9f464d131615c6d831680ad93160d93396`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e4e71c2dd1e003a55d7d71bb9605962da10a0fe01ab4389c7ed73d3554004`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96448d3612a0568a7546321726cc4614b4660669dbcb013d84927f3e5d46044c`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ac485df781b5855a726f9a564247f671b05307b9a60d7edc47fe5fa4ddd59179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4fb44125c8deb9411165816461a05957a0ba9fdb1392107b8189bc4c8a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:5eed377ab5863f68540f4fdf25e5f6115c22cea7a09d6fd2a5f397fe71cbc0ac`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.0 MB (3954775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21933d6ce644b261242766852efeea75729d4372bd091955a5bd3f41798b2ed6`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:92923e99278839ae86ba3edde972cf46f620ada05b37f85db04398cf8d7fc2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9aa790f95200ad044e57741ad3b23ef8b396d4be7ae85b4b8696c9bbc7168b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174790853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f309f7dabfd1bb9a6f8ce65028d1fc1636074e4463676580894e5b59af10c4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09b1c7d50d0745c852e3f217b873c881e4573e8d482fdf12e07cae62461b97`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a6697daf1314aef2e087deadaa18e37fee5b2d1044569bf7c4ee700e5d123`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f40b0c53d71d13804fba188a21df731aa9ada6cf0ba757ef1638030ed7039c`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 4.6 MB (4607397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fdbb420ffeea98a18e309057fbb3b3a93157947eb7a9b610e02ccf0b88b9a`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964da5c649e204b4fb39c391ee0a9cdaa0e99dda9bbb4710a4d6cf86e1d673dd`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd68fed930245b826c61227ba6656e8f67463016b85c66ef658bcf057119744`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 58.5 MB (58529828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f88f90d943bbaf7143ec068d33df13c22e37019667234fee196dd3bc72b3d3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9e6ae336c3aa275cccadc6f2fa6df826424c19d8ddb96f320866b0e5788c3`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 59.3 MB (59333952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3624bb597fc3508d4c21b075ad07b46c2252da9a92a1235093b343dbf6a421`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5c5a90ca7f47acc73cc8db3d9e47a4a6a55a29f57e42820f8ec78fe7598ed`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:570f9b1f56a0f792e296d72a362dcc0874e29d11fe6d251d354a1ea5c5c6b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de4182006b637eafd896bc623ec2b30695e0cf68ea9169df4021da1b47672b`

```dockerfile
```

-	Layers:
	-	`sha256:f742d61ef088a638e7c67a6585099be1b7987149874f9b2b7f7d4ac4cbd44da8`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 14.2 MB (14248912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2bd61f95a481fb980f77c2b1474b462a544dfa1f4c8d16eb3dd89b9f78ded8`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26df16d3c97cc9142b77402aa8d29418e98b073dc3a692738f0a5ae3e647d90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178451913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73c6e55254408fd327a42eefb5477d001c395b6a9a260379c96b645db52301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf5f8b6640146cdb4a35578f6a3e8f4e8b48f03c870f8187c4c79909771378`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdeddc397e162f8ca0732bbb6c994ecd3098d6fdc2b37691acf4f07f6ade95`  
		Last Modified: Wed, 14 Feb 2024 11:02:27 GMT  
		Size: 57.6 MB (57579757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51065c28a837882374674779bc906cd6f6350b15ca440863c760b60885aaa93e`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bd88fdeb3df2956cdbdca413b27546d8cdece2d0a4656e3c0d31a0efa255f`  
		Last Modified: Wed, 14 Feb 2024 11:02:26 GMT  
		Size: 65.6 MB (65580430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242e8cb8356c83f92af998acbf475f04ca5794948510d561d5d4405c396b184`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2629cfe75be9f6fda271ec2ab14026f96f570f8b3a4ac0c669669a9e94bfc`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71bd429485fbd27de87bc6df70171585bab325ba725fe33f41638d2a28e5c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64716502b2bee010019f103bd457ed7c4d2c0c8a79ab2e1cf9d002f745509324`

```dockerfile
```

-	Layers:
	-	`sha256:80ae47d0d6b69d63962cc882f027a0d561c20514fbea063ba66f16374725564b`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be015ae2a767b85f837175108bc9c2e71cf8e05064cc9e68e5c58c02e6cda6a`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux8`

```console
$ docker pull mysql@sha256:92923e99278839ae86ba3edde972cf46f620ada05b37f85db04398cf8d7fc2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:9aa790f95200ad044e57741ad3b23ef8b396d4be7ae85b4b8696c9bbc7168b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174790853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f309f7dabfd1bb9a6f8ce65028d1fc1636074e4463676580894e5b59af10c4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09b1c7d50d0745c852e3f217b873c881e4573e8d482fdf12e07cae62461b97`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a6697daf1314aef2e087deadaa18e37fee5b2d1044569bf7c4ee700e5d123`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f40b0c53d71d13804fba188a21df731aa9ada6cf0ba757ef1638030ed7039c`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 4.6 MB (4607397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fdbb420ffeea98a18e309057fbb3b3a93157947eb7a9b610e02ccf0b88b9a`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964da5c649e204b4fb39c391ee0a9cdaa0e99dda9bbb4710a4d6cf86e1d673dd`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd68fed930245b826c61227ba6656e8f67463016b85c66ef658bcf057119744`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 58.5 MB (58529828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f88f90d943bbaf7143ec068d33df13c22e37019667234fee196dd3bc72b3d3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9e6ae336c3aa275cccadc6f2fa6df826424c19d8ddb96f320866b0e5788c3`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 59.3 MB (59333952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3624bb597fc3508d4c21b075ad07b46c2252da9a92a1235093b343dbf6a421`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5c5a90ca7f47acc73cc8db3d9e47a4a6a55a29f57e42820f8ec78fe7598ed`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:570f9b1f56a0f792e296d72a362dcc0874e29d11fe6d251d354a1ea5c5c6b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de4182006b637eafd896bc623ec2b30695e0cf68ea9169df4021da1b47672b`

```dockerfile
```

-	Layers:
	-	`sha256:f742d61ef088a638e7c67a6585099be1b7987149874f9b2b7f7d4ac4cbd44da8`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 14.2 MB (14248912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2bd61f95a481fb980f77c2b1474b462a544dfa1f4c8d16eb3dd89b9f78ded8`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26df16d3c97cc9142b77402aa8d29418e98b073dc3a692738f0a5ae3e647d90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178451913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73c6e55254408fd327a42eefb5477d001c395b6a9a260379c96b645db52301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf5f8b6640146cdb4a35578f6a3e8f4e8b48f03c870f8187c4c79909771378`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdeddc397e162f8ca0732bbb6c994ecd3098d6fdc2b37691acf4f07f6ade95`  
		Last Modified: Wed, 14 Feb 2024 11:02:27 GMT  
		Size: 57.6 MB (57579757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51065c28a837882374674779bc906cd6f6350b15ca440863c760b60885aaa93e`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bd88fdeb3df2956cdbdca413b27546d8cdece2d0a4656e3c0d31a0efa255f`  
		Last Modified: Wed, 14 Feb 2024 11:02:26 GMT  
		Size: 65.6 MB (65580430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242e8cb8356c83f92af998acbf475f04ca5794948510d561d5d4405c396b184`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2629cfe75be9f6fda271ec2ab14026f96f570f8b3a4ac0c669669a9e94bfc`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:71bd429485fbd27de87bc6df70171585bab325ba725fe33f41638d2a28e5c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64716502b2bee010019f103bd457ed7c4d2c0c8a79ab2e1cf9d002f745509324`

```dockerfile
```

-	Layers:
	-	`sha256:80ae47d0d6b69d63962cc882f027a0d561c20514fbea063ba66f16374725564b`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be015ae2a767b85f837175108bc9c2e71cf8e05064cc9e68e5c58c02e6cda6a`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36`

```console
$ docker pull mysql@sha256:92923e99278839ae86ba3edde972cf46f620ada05b37f85db04398cf8d7fc2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36` - linux; amd64

```console
$ docker pull mysql@sha256:9aa790f95200ad044e57741ad3b23ef8b396d4be7ae85b4b8696c9bbc7168b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174790853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f309f7dabfd1bb9a6f8ce65028d1fc1636074e4463676580894e5b59af10c4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09b1c7d50d0745c852e3f217b873c881e4573e8d482fdf12e07cae62461b97`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a6697daf1314aef2e087deadaa18e37fee5b2d1044569bf7c4ee700e5d123`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f40b0c53d71d13804fba188a21df731aa9ada6cf0ba757ef1638030ed7039c`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 4.6 MB (4607397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fdbb420ffeea98a18e309057fbb3b3a93157947eb7a9b610e02ccf0b88b9a`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964da5c649e204b4fb39c391ee0a9cdaa0e99dda9bbb4710a4d6cf86e1d673dd`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd68fed930245b826c61227ba6656e8f67463016b85c66ef658bcf057119744`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 58.5 MB (58529828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f88f90d943bbaf7143ec068d33df13c22e37019667234fee196dd3bc72b3d3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9e6ae336c3aa275cccadc6f2fa6df826424c19d8ddb96f320866b0e5788c3`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 59.3 MB (59333952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3624bb597fc3508d4c21b075ad07b46c2252da9a92a1235093b343dbf6a421`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5c5a90ca7f47acc73cc8db3d9e47a4a6a55a29f57e42820f8ec78fe7598ed`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:570f9b1f56a0f792e296d72a362dcc0874e29d11fe6d251d354a1ea5c5c6b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de4182006b637eafd896bc623ec2b30695e0cf68ea9169df4021da1b47672b`

```dockerfile
```

-	Layers:
	-	`sha256:f742d61ef088a638e7c67a6585099be1b7987149874f9b2b7f7d4ac4cbd44da8`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 14.2 MB (14248912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2bd61f95a481fb980f77c2b1474b462a544dfa1f4c8d16eb3dd89b9f78ded8`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26df16d3c97cc9142b77402aa8d29418e98b073dc3a692738f0a5ae3e647d90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178451913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73c6e55254408fd327a42eefb5477d001c395b6a9a260379c96b645db52301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf5f8b6640146cdb4a35578f6a3e8f4e8b48f03c870f8187c4c79909771378`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdeddc397e162f8ca0732bbb6c994ecd3098d6fdc2b37691acf4f07f6ade95`  
		Last Modified: Wed, 14 Feb 2024 11:02:27 GMT  
		Size: 57.6 MB (57579757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51065c28a837882374674779bc906cd6f6350b15ca440863c760b60885aaa93e`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bd88fdeb3df2956cdbdca413b27546d8cdece2d0a4656e3c0d31a0efa255f`  
		Last Modified: Wed, 14 Feb 2024 11:02:26 GMT  
		Size: 65.6 MB (65580430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242e8cb8356c83f92af998acbf475f04ca5794948510d561d5d4405c396b184`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2629cfe75be9f6fda271ec2ab14026f96f570f8b3a4ac0c669669a9e94bfc`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36` - unknown; unknown

```console
$ docker pull mysql@sha256:71bd429485fbd27de87bc6df70171585bab325ba725fe33f41638d2a28e5c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64716502b2bee010019f103bd457ed7c4d2c0c8a79ab2e1cf9d002f745509324`

```dockerfile
```

-	Layers:
	-	`sha256:80ae47d0d6b69d63962cc882f027a0d561c20514fbea063ba66f16374725564b`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be015ae2a767b85f837175108bc9c2e71cf8e05064cc9e68e5c58c02e6cda6a`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-bookworm`

```console
$ docker pull mysql@sha256:b64e2d58cc179e38acb0ccdae5a5a91368f93a00fef422ed34cf6a698e1c0d32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:cfb4769acf1cd2945a83f401810a12883a905d148b6f01f8b739d46809b5af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180826047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e09efbec746077116fffe18e56f6af97f369d8aec7868226048248ca2fff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 21:25:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV GOSU_VERSION=1.16
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Wed, 28 Feb 2024 21:25:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Feb 2024 21:25:11 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 21:25:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Feb 2024 21:25:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93500000d2237d1a816fbad4d4d96c74914a325c087554b804c977d52b12d0`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca73a9485b2e290356558877f1aac55608843603177fe71830317451c0c38eb6`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.4 MB (4422794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc655ca6ff77811573539289d01ffdf3f02b46002efb715aab3391cbb9a0689`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.4 MB (1445462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099440dd6678c36a1c79ea9f8af24dcfb826128159dee2273f9ccb7fbee184f9`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d32c3d97d54b2b2994d7f203c7d31276afeb633bf49a3a923f7d6f2abc8b2`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 15.3 MB (15281620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038b55db03e70b5044da4ab6e7a0b4b2839d81f119499eadc2530d46f50f68f5`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e3b64441767050d3e4ef7303a90b1b1f8316cd576f5c03849ba4df0622b4cc`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3fd9fe1c53d7035167e80161764c3f1f32ea0f8e848d05b8b195ea7cadc024`  
		Last Modified: Thu, 29 Feb 2024 19:49:55 GMT  
		Size: 130.5 MB (130541962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d966ddd4cb66db76e594361804b9af9f464d131615c6d831680ad93160d93396`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e4e71c2dd1e003a55d7d71bb9605962da10a0fe01ab4389c7ed73d3554004`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96448d3612a0568a7546321726cc4614b4660669dbcb013d84927f3e5d46044c`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ac485df781b5855a726f9a564247f671b05307b9a60d7edc47fe5fa4ddd59179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4fb44125c8deb9411165816461a05957a0ba9fdb1392107b8189bc4c8a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:5eed377ab5863f68540f4fdf25e5f6115c22cea7a09d6fd2a5f397fe71cbc0ac`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.0 MB (3954775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21933d6ce644b261242766852efeea75729d4372bd091955a5bd3f41798b2ed6`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-debian`

```console
$ docker pull mysql@sha256:b64e2d58cc179e38acb0ccdae5a5a91368f93a00fef422ed34cf6a698e1c0d32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.36-debian` - linux; amd64

```console
$ docker pull mysql@sha256:cfb4769acf1cd2945a83f401810a12883a905d148b6f01f8b739d46809b5af9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180826047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:384e09efbec746077116fffe18e56f6af97f369d8aec7868226048248ca2fff3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Wed, 28 Feb 2024 21:25:11 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV GOSU_VERSION=1.16
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 28 Feb 2024 21:25:11 GMT
ENV MYSQL_VERSION=8.0.36-1debian12
# Wed, 28 Feb 2024 21:25:11 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
VOLUME [/var/lib/mysql]
# Wed, 28 Feb 2024 21:25:11 GMT
COPY config/ /etc/mysql/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 28 Feb 2024 21:25:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 28 Feb 2024 21:25:11 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 28 Feb 2024 21:25:11 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a93500000d2237d1a816fbad4d4d96c74914a325c087554b804c977d52b12d0`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca73a9485b2e290356558877f1aac55608843603177fe71830317451c0c38eb6`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.4 MB (4422794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc655ca6ff77811573539289d01ffdf3f02b46002efb715aab3391cbb9a0689`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 1.4 MB (1445462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099440dd6678c36a1c79ea9f8af24dcfb826128159dee2273f9ccb7fbee184f9`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d32c3d97d54b2b2994d7f203c7d31276afeb633bf49a3a923f7d6f2abc8b2`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 15.3 MB (15281620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038b55db03e70b5044da4ab6e7a0b4b2839d81f119499eadc2530d46f50f68f5`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 2.5 KB (2505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e3b64441767050d3e4ef7303a90b1b1f8316cd576f5c03849ba4df0622b4cc`  
		Last Modified: Thu, 29 Feb 2024 19:49:51 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3fd9fe1c53d7035167e80161764c3f1f32ea0f8e848d05b8b195ea7cadc024`  
		Last Modified: Thu, 29 Feb 2024 19:49:55 GMT  
		Size: 130.5 MB (130541962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d966ddd4cb66db76e594361804b9af9f464d131615c6d831680ad93160d93396`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 842.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e4e71c2dd1e003a55d7d71bb9605962da10a0fe01ab4389c7ed73d3554004`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 5.2 KB (5174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96448d3612a0568a7546321726cc4614b4660669dbcb013d84927f3e5d46044c`  
		Last Modified: Thu, 29 Feb 2024 19:49:52 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ac485df781b5855a726f9a564247f671b05307b9a60d7edc47fe5fa4ddd59179
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3989026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d4fb44125c8deb9411165816461a05957a0ba9fdb1392107b8189bc4c8a9c6`

```dockerfile
```

-	Layers:
	-	`sha256:5eed377ab5863f68540f4fdf25e5f6115c22cea7a09d6fd2a5f397fe71cbc0ac`  
		Last Modified: Thu, 29 Feb 2024 19:49:50 GMT  
		Size: 4.0 MB (3954775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21933d6ce644b261242766852efeea75729d4372bd091955a5bd3f41798b2ed6`  
		Last Modified: Thu, 29 Feb 2024 19:49:49 GMT  
		Size: 34.3 KB (34251 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oracle`

```console
$ docker pull mysql@sha256:92923e99278839ae86ba3edde972cf46f620ada05b37f85db04398cf8d7fc2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9aa790f95200ad044e57741ad3b23ef8b396d4be7ae85b4b8696c9bbc7168b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174790853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f309f7dabfd1bb9a6f8ce65028d1fc1636074e4463676580894e5b59af10c4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09b1c7d50d0745c852e3f217b873c881e4573e8d482fdf12e07cae62461b97`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a6697daf1314aef2e087deadaa18e37fee5b2d1044569bf7c4ee700e5d123`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f40b0c53d71d13804fba188a21df731aa9ada6cf0ba757ef1638030ed7039c`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 4.6 MB (4607397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fdbb420ffeea98a18e309057fbb3b3a93157947eb7a9b610e02ccf0b88b9a`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964da5c649e204b4fb39c391ee0a9cdaa0e99dda9bbb4710a4d6cf86e1d673dd`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd68fed930245b826c61227ba6656e8f67463016b85c66ef658bcf057119744`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 58.5 MB (58529828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f88f90d943bbaf7143ec068d33df13c22e37019667234fee196dd3bc72b3d3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9e6ae336c3aa275cccadc6f2fa6df826424c19d8ddb96f320866b0e5788c3`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 59.3 MB (59333952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3624bb597fc3508d4c21b075ad07b46c2252da9a92a1235093b343dbf6a421`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5c5a90ca7f47acc73cc8db3d9e47a4a6a55a29f57e42820f8ec78fe7598ed`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:570f9b1f56a0f792e296d72a362dcc0874e29d11fe6d251d354a1ea5c5c6b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de4182006b637eafd896bc623ec2b30695e0cf68ea9169df4021da1b47672b`

```dockerfile
```

-	Layers:
	-	`sha256:f742d61ef088a638e7c67a6585099be1b7987149874f9b2b7f7d4ac4cbd44da8`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 14.2 MB (14248912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2bd61f95a481fb980f77c2b1474b462a544dfa1f4c8d16eb3dd89b9f78ded8`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26df16d3c97cc9142b77402aa8d29418e98b073dc3a692738f0a5ae3e647d90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178451913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73c6e55254408fd327a42eefb5477d001c395b6a9a260379c96b645db52301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf5f8b6640146cdb4a35578f6a3e8f4e8b48f03c870f8187c4c79909771378`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdeddc397e162f8ca0732bbb6c994ecd3098d6fdc2b37691acf4f07f6ade95`  
		Last Modified: Wed, 14 Feb 2024 11:02:27 GMT  
		Size: 57.6 MB (57579757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51065c28a837882374674779bc906cd6f6350b15ca440863c760b60885aaa93e`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bd88fdeb3df2956cdbdca413b27546d8cdece2d0a4656e3c0d31a0efa255f`  
		Last Modified: Wed, 14 Feb 2024 11:02:26 GMT  
		Size: 65.6 MB (65580430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242e8cb8356c83f92af998acbf475f04ca5794948510d561d5d4405c396b184`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2629cfe75be9f6fda271ec2ab14026f96f570f8b3a4ac0c669669a9e94bfc`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:71bd429485fbd27de87bc6df70171585bab325ba725fe33f41638d2a28e5c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64716502b2bee010019f103bd457ed7c4d2c0c8a79ab2e1cf9d002f745509324`

```dockerfile
```

-	Layers:
	-	`sha256:80ae47d0d6b69d63962cc882f027a0d561c20514fbea063ba66f16374725564b`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be015ae2a767b85f837175108bc9c2e71cf8e05064cc9e68e5c58c02e6cda6a`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.36-oraclelinux8`

```console
$ docker pull mysql@sha256:92923e99278839ae86ba3edde972cf46f620ada05b37f85db04398cf8d7fc2b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.36-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:9aa790f95200ad044e57741ad3b23ef8b396d4be7ae85b4b8696c9bbc7168b38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174790853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f309f7dabfd1bb9a6f8ce65028d1fc1636074e4463676580894e5b59af10c4ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c09b1c7d50d0745c852e3f217b873c881e4573e8d482fdf12e07cae62461b97`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d5a6697daf1314aef2e087deadaa18e37fee5b2d1044569bf7c4ee700e5d123`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f40b0c53d71d13804fba188a21df731aa9ada6cf0ba757ef1638030ed7039c`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 4.6 MB (4607397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6fdbb420ffeea98a18e309057fbb3b3a93157947eb7a9b610e02ccf0b88b9a`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964da5c649e204b4fb39c391ee0a9cdaa0e99dda9bbb4710a4d6cf86e1d673dd`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd68fed930245b826c61227ba6656e8f67463016b85c66ef658bcf057119744`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 58.5 MB (58529828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f88f90d943bbaf7143ec068d33df13c22e37019667234fee196dd3bc72b3d3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d9e6ae336c3aa275cccadc6f2fa6df826424c19d8ddb96f320866b0e5788c3`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 59.3 MB (59333952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3624bb597fc3508d4c21b075ad07b46c2252da9a92a1235093b343dbf6a421`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba5c5a90ca7f47acc73cc8db3d9e47a4a6a55a29f57e42820f8ec78fe7598ed`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:570f9b1f56a0f792e296d72a362dcc0874e29d11fe6d251d354a1ea5c5c6b520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14283807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80de4182006b637eafd896bc623ec2b30695e0cf68ea9169df4021da1b47672b`

```dockerfile
```

-	Layers:
	-	`sha256:f742d61ef088a638e7c67a6585099be1b7987149874f9b2b7f7d4ac4cbd44da8`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 14.2 MB (14248912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c2bd61f95a481fb980f77c2b1474b462a544dfa1f4c8d16eb3dd89b9f78ded8`  
		Last Modified: Fri, 08 Mar 2024 19:50:27 GMT  
		Size: 34.9 KB (34895 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.36-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:26df16d3c97cc9142b77402aa8d29418e98b073dc3a692738f0a5ae3e647d90b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178451913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e73c6e55254408fd327a42eefb5477d001c395b6a9a260379c96b645db52301`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=8.0
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.0.36-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cf5f8b6640146cdb4a35578f6a3e8f4e8b48f03c870f8187c4c79909771378`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecdeddc397e162f8ca0732bbb6c994ecd3098d6fdc2b37691acf4f07f6ade95`  
		Last Modified: Wed, 14 Feb 2024 11:02:27 GMT  
		Size: 57.6 MB (57579757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51065c28a837882374674779bc906cd6f6350b15ca440863c760b60885aaa93e`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801bd88fdeb3df2956cdbdca413b27546d8cdece2d0a4656e3c0d31a0efa255f`  
		Last Modified: Wed, 14 Feb 2024 11:02:26 GMT  
		Size: 65.6 MB (65580430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f242e8cb8356c83f92af998acbf475f04ca5794948510d561d5d4405c396b184`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 5.2 KB (5178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c2629cfe75be9f6fda271ec2ab14026f96f570f8b3a4ac0c669669a9e94bfc`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.36-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:71bd429485fbd27de87bc6df70171585bab325ba725fe33f41638d2a28e5c48a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12161386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64716502b2bee010019f103bd457ed7c4d2c0c8a79ab2e1cf9d002f745509324`

```dockerfile
```

-	Layers:
	-	`sha256:80ae47d0d6b69d63962cc882f027a0d561c20514fbea063ba66f16374725564b`  
		Last Modified: Wed, 14 Feb 2024 11:02:24 GMT  
		Size: 12.1 MB (12126644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6be015ae2a767b85f837175108bc9c2e71cf8e05064cc9e68e5c58c02e6cda6a`  
		Last Modified: Wed, 14 Feb 2024 11:02:23 GMT  
		Size: 34.7 KB (34742 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oracle`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3-oraclelinux8`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oracle`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.3.0-oraclelinux8`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.3.0-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.3.0-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.3.0-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux8`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux8`

```console
$ docker pull mysql@sha256:9d1c923e5f66a89607285ee2641f8a53430a1ccd5e4a62b35eb8a48b74b9ff48
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux8` - linux; amd64

```console
$ docker pull mysql@sha256:eeabfa5cd6a2091bf35eb9eae6ae48aab8231fd760f5a61cd0129df454333b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183440024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:019814493c7ab16a057af0399b1288a1208b75ba852b915541840095c0fedfd0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:5b9f2edfe5330237c32cbb7de3fd4ea6ff66741feadb0d181acd63abb9fb5e7c in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:9a5c778f631f809e7c73d260001cedbcd41156ec483a8321169ed2ff5f395e7e`  
		Last Modified: Fri, 08 Mar 2024 19:23:04 GMT  
		Size: 51.3 MB (51327420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e77c3a95bf244837ef3176e72e05de7ec1d014ef3a1a76c9030016f9013f047`  
		Last Modified: Fri, 08 Mar 2024 19:50:28 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b279a2086e00211e98e27d35c4fde07bb0b4c25ea9b49a4c6bafbe489e4bcd4`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 982.8 KB (982810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bfbcde78826dc45fa2e00e48e5a0741b73d0ae60f7d8730aa48985af5832c5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 4.6 MB (4607369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35b074b68ec4634aec857bc99877e4c74b828f5c9d11f53ef034847f09262e5`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beea5014e6afeae9ff205e80d71a77fcff7c97e39aa7a143fc80452c759a6c6c`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3791a61558d7758d9e9b0dc0b83b1d85f4c46b52ec9f0ba5bbefdcf98ba6e6`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.1 MB (63093875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f9323b9f0e9f41d474a790a61a9564bf7dd4568558ff259668b44ad28de3b1`  
		Last Modified: Fri, 08 Mar 2024 19:50:30 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7391eab49be09805709ed6f59591af2e8117478bbf07407a33147993b5b148`  
		Last Modified: Fri, 08 Mar 2024 19:50:32 GMT  
		Size: 63.4 MB (63419208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2f04b287ee751034e7ce212ee82abdfc4980faac13cb8627f916b3b268d93e`  
		Last Modified: Fri, 08 Mar 2024 19:50:31 GMT  
		Size: 5.2 KB (5182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:88da9eaf220c976f76ce899a778bdcf0903c5cb334642551129100281dda34a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.3 MB (14287264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e72cc37ca916c71906c35b179e686d535917b5fea8aae85ceb445df88a97b9b`

```dockerfile
```

-	Layers:
	-	`sha256:da913236dd60a694478dd288273763675c2d5fd16fcebe48f5d5620dc62492b3`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 14.3 MB (14252010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a92219d33adf98def615c71489ec87651ac9aecd930144d6f8e9d751c15187d`  
		Last Modified: Fri, 08 Mar 2024 19:50:29 GMT  
		Size: 35.3 KB (35254 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:cf2ece69590c9306aea19dbcc6880fd2f839378b5a0599fc2144d8fd53d7c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181350870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e68e2614955cad9955f5bf3eab032c5c5356e00ae1e7725e850cc0beec446214`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 18 Jan 2024 17:37:32 GMT
ADD file:53c58659a3a149d31f0d4d27fa4b6bd9309fb3d49af7029f3734b7412be59e5b in / 
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["/bin/bash"]
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV GOSU_VERSION=1.16
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_MAJOR=innovation
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/8/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/8/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENV MYSQL_SHELL_VERSION=8.3.0-1.el8
# Thu, 18 Jan 2024 17:37:32 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
VOLUME [/var/lib/mysql]
# Thu, 18 Jan 2024 17:37:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jan 2024 17:37:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jan 2024 17:37:32 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Thu, 18 Jan 2024 17:37:32 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:ea4e27ae0b4ca9ec65ab9fad027fde7a9b423d8982124bf17fee78d70c56715d`  
		Last Modified: Wed, 14 Feb 2024 01:46:25 GMT  
		Size: 50.1 MB (50072914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83790430248242651bf0fd628da54a6ba6285193bbb5b6dd885276c30dda0fca`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c574b61b2411bc88f41515e3cb0e2adea26cecbbf09f08c8629993e67e17fe1`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 913.0 KB (912965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654fc4f3eb2d8d40b8cb0624d941ee572357f12bee608d47db41c249b5514964`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 4.3 MB (4296411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32da9c2187e392ab929fab14fb34c690b1bc9fd1b57328427bba8d7be8157b5c`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99c3c88bd6a34b9545aaf31cc887e6593c8de6b75462e970c17b6f719d7033`  
		Last Modified: Wed, 14 Feb 2024 11:00:32 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970181cc0aa652b91de7ef5d3a4a8334ca1aa33ba6c056d9e40b3393c55f8e7a`  
		Last Modified: Wed, 14 Feb 2024 11:00:35 GMT  
		Size: 62.0 MB (62038818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77b716c39d5b0ea63d0ceede4cf7561556f433b87b57469ffb08dfff917341a`  
		Last Modified: Wed, 14 Feb 2024 11:00:33 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e650d7f9f83be21b6573f6e6928f6feca92eeda8d3fff9b87ce692342008aaf`  
		Last Modified: Wed, 14 Feb 2024 11:00:36 GMT  
		Size: 64.0 MB (64020429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc21ff36b4b883c5f94497fb34e8b488b8fc405d527d4fa78eb88716f04a150`  
		Last Modified: Wed, 14 Feb 2024 11:00:34 GMT  
		Size: 5.2 KB (5181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux8` - unknown; unknown

```console
$ docker pull mysql@sha256:2992bb8f887541d31fd2620bca3517c79493d221c2e574237eccb197f2c6f044
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.2 MB (12164939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d943f63e9e568384c0c1fd4311e13ef90099e33afefef87dd105743d4594af20`

```dockerfile
```

-	Layers:
	-	`sha256:4d1c8b0d984b5d7fdeeade25631416d5bf469b14276110d512cb50e74d30823a`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 12.1 MB (12129654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd46473e3d612a62cf79ea1ac033c73ba240026e52911972dc2808d3aa221dc`  
		Last Modified: Wed, 14 Feb 2024 11:00:31 GMT  
		Size: 35.3 KB (35285 bytes)  
		MIME: application/vnd.in-toto+json
