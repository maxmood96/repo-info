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
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:0f34c70018dcbde655ba3eaba3d33c02198d392b9364974462eee13a903af385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:e778ad05466b7b12d6cbd13467271eb5ddad447bb676f79f9d1ab56572bb3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232285671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be417a60070a28d3b5e1db55800e358dcb8102083e2d587151fa58d98e785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:11:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:11:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd727943cf78a9f0ad1b104f4428b176dbb0279a5b1e92089efeb876948241`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183dada878863ad480368d0146eef3f2a4a01333f0ebd79c92116d5706977ca4`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca475193795ea762124043003f042cc6a5c2669294f0634add4d91f3e448d702`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 6.2 MB (6171304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a6efc32c61af1ae1fe48c1f8ea3ff872c21ce735ca8275edcc5255215f94a`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf107c1a2b33832ab078177d32f4b73961548ef7ce317b7ce7f0031e0db02193`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc630d3abcacff776255b4dfc25973c9af312598c15a6e3b43f17ab5261527`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 49.9 MB (49918946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b8625e4a373abd821788926da90e75cdaf2fc3a074a1b6587ef55834e8a6`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1297c1feceb7dd03edce7bb869223443cb6bf4517b8373c26a3bd6bb9bde9de`  
		Last Modified: Fri, 13 Mar 2026 23:13:19 GMT  
		Size: 128.1 MB (128098070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177fa0193b5c264d9f965d7bbedb4b16519340b616023ab19e6919986508781b`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122248aa49cd9e45c67433da6a74d9f8a81f317a6ede6a90092273b5a58e182`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:faade5acdd2acf4671ec95417e06ccc5ee4916d908080eded8c67b04e6b0b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51fa88745b7012cae4447bc76c389af4474dd79b2579d4ba8c50ad76feb700`

```dockerfile
```

-	Layers:
	-	`sha256:3330278a99c6d8715d2e22bde8ea5f89f5f5fb95534ac52e45424a8fab73c1fd`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d7465fe0a62b25696717b40ffb7aed5e4e5942145b573f0fc1cc612f8b11c`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d893ded57f82bb14cfe8258a8b49cf221e7e4b7581cc468f41564ebafa8017fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227906178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3bfc161a3c10708fc3e08c76b6ea7b7a3086212cbe8a2881593dab49b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:42 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39676fe8009672ced14ffa7e0d527ebdcfcd9909c02afbc97204fce62c41b77c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bca3b1a4681080d56d50fed1bc9ecc03c7eba0fb5558ce3533a8236ed1fc0c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8816a4545c8dd7279d6bd4d074560ce2b6769a3f98f8793d59ab322bd160ce4d`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 5.8 MB (5793597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab8f2de72f76a5f06196be92502620b578a4d358abcf93c5001b9ed3f32c1f`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79772aa74f1eae8ab8161d412141da67c1f7e7aaa398bcc9ae5043a4d596baf`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34007679fce091d3203b832c87b8f4c3d1c2809de5d7434c9d4036fd9bf98c`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 48.8 MB (48779936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e64b1ca3afd709e94aeec39594758aa1dd05e3f0a35b8e7dd7f33b93257d0a5`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae051ab9e6ff361121ac03f3b7391251e50a23033d5b50103609665abb866517`  
		Last Modified: Fri, 13 Mar 2026 23:12:53 GMT  
		Size: 126.7 MB (126685350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee96801673cf73a413bd74e781dac7f1729460f1a22c425d589ebf58a4f5d02`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0a95555d23e2e68e0faa2325a2f8ee25e2e48d492e4e72a8d2bf669f0574`  
		Last Modified: Fri, 13 Mar 2026 23:12:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:8c75b94498a1631870b6bd71639f085345a27e2640b764ad37dab15472c7f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e042e80ea3c659632dd81daf530d619cd3f64035d18e128c206019653b50d`

```dockerfile
```

-	Layers:
	-	`sha256:81fda180811778da47155c0eb93e4a7ee7a6387191a312311e09e4b31285017e`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb736ecc0aa188c4abee2c00270f9ad0979736078c07637257a7abce00ef3fc`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:0f34c70018dcbde655ba3eaba3d33c02198d392b9364974462eee13a903af385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e778ad05466b7b12d6cbd13467271eb5ddad447bb676f79f9d1ab56572bb3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232285671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be417a60070a28d3b5e1db55800e358dcb8102083e2d587151fa58d98e785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:11:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:11:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd727943cf78a9f0ad1b104f4428b176dbb0279a5b1e92089efeb876948241`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183dada878863ad480368d0146eef3f2a4a01333f0ebd79c92116d5706977ca4`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca475193795ea762124043003f042cc6a5c2669294f0634add4d91f3e448d702`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 6.2 MB (6171304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a6efc32c61af1ae1fe48c1f8ea3ff872c21ce735ca8275edcc5255215f94a`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf107c1a2b33832ab078177d32f4b73961548ef7ce317b7ce7f0031e0db02193`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc630d3abcacff776255b4dfc25973c9af312598c15a6e3b43f17ab5261527`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 49.9 MB (49918946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b8625e4a373abd821788926da90e75cdaf2fc3a074a1b6587ef55834e8a6`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1297c1feceb7dd03edce7bb869223443cb6bf4517b8373c26a3bd6bb9bde9de`  
		Last Modified: Fri, 13 Mar 2026 23:13:19 GMT  
		Size: 128.1 MB (128098070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177fa0193b5c264d9f965d7bbedb4b16519340b616023ab19e6919986508781b`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122248aa49cd9e45c67433da6a74d9f8a81f317a6ede6a90092273b5a58e182`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:faade5acdd2acf4671ec95417e06ccc5ee4916d908080eded8c67b04e6b0b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51fa88745b7012cae4447bc76c389af4474dd79b2579d4ba8c50ad76feb700`

```dockerfile
```

-	Layers:
	-	`sha256:3330278a99c6d8715d2e22bde8ea5f89f5f5fb95534ac52e45424a8fab73c1fd`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d7465fe0a62b25696717b40ffb7aed5e4e5942145b573f0fc1cc612f8b11c`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d893ded57f82bb14cfe8258a8b49cf221e7e4b7581cc468f41564ebafa8017fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227906178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3bfc161a3c10708fc3e08c76b6ea7b7a3086212cbe8a2881593dab49b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:42 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39676fe8009672ced14ffa7e0d527ebdcfcd9909c02afbc97204fce62c41b77c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bca3b1a4681080d56d50fed1bc9ecc03c7eba0fb5558ce3533a8236ed1fc0c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8816a4545c8dd7279d6bd4d074560ce2b6769a3f98f8793d59ab322bd160ce4d`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 5.8 MB (5793597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab8f2de72f76a5f06196be92502620b578a4d358abcf93c5001b9ed3f32c1f`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79772aa74f1eae8ab8161d412141da67c1f7e7aaa398bcc9ae5043a4d596baf`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34007679fce091d3203b832c87b8f4c3d1c2809de5d7434c9d4036fd9bf98c`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 48.8 MB (48779936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e64b1ca3afd709e94aeec39594758aa1dd05e3f0a35b8e7dd7f33b93257d0a5`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae051ab9e6ff361121ac03f3b7391251e50a23033d5b50103609665abb866517`  
		Last Modified: Fri, 13 Mar 2026 23:12:53 GMT  
		Size: 126.7 MB (126685350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee96801673cf73a413bd74e781dac7f1729460f1a22c425d589ebf58a4f5d02`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0a95555d23e2e68e0faa2325a2f8ee25e2e48d492e4e72a8d2bf669f0574`  
		Last Modified: Fri, 13 Mar 2026 23:12:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8c75b94498a1631870b6bd71639f085345a27e2640b764ad37dab15472c7f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e042e80ea3c659632dd81daf530d619cd3f64035d18e128c206019653b50d`

```dockerfile
```

-	Layers:
	-	`sha256:81fda180811778da47155c0eb93e4a7ee7a6387191a312311e09e4b31285017e`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb736ecc0aa188c4abee2c00270f9ad0979736078c07637257a7abce00ef3fc`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:0f34c70018dcbde655ba3eaba3d33c02198d392b9364974462eee13a903af385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e778ad05466b7b12d6cbd13467271eb5ddad447bb676f79f9d1ab56572bb3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232285671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be417a60070a28d3b5e1db55800e358dcb8102083e2d587151fa58d98e785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:11:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:11:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd727943cf78a9f0ad1b104f4428b176dbb0279a5b1e92089efeb876948241`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183dada878863ad480368d0146eef3f2a4a01333f0ebd79c92116d5706977ca4`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca475193795ea762124043003f042cc6a5c2669294f0634add4d91f3e448d702`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 6.2 MB (6171304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a6efc32c61af1ae1fe48c1f8ea3ff872c21ce735ca8275edcc5255215f94a`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf107c1a2b33832ab078177d32f4b73961548ef7ce317b7ce7f0031e0db02193`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc630d3abcacff776255b4dfc25973c9af312598c15a6e3b43f17ab5261527`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 49.9 MB (49918946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b8625e4a373abd821788926da90e75cdaf2fc3a074a1b6587ef55834e8a6`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1297c1feceb7dd03edce7bb869223443cb6bf4517b8373c26a3bd6bb9bde9de`  
		Last Modified: Fri, 13 Mar 2026 23:13:19 GMT  
		Size: 128.1 MB (128098070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177fa0193b5c264d9f965d7bbedb4b16519340b616023ab19e6919986508781b`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122248aa49cd9e45c67433da6a74d9f8a81f317a6ede6a90092273b5a58e182`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:faade5acdd2acf4671ec95417e06ccc5ee4916d908080eded8c67b04e6b0b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51fa88745b7012cae4447bc76c389af4474dd79b2579d4ba8c50ad76feb700`

```dockerfile
```

-	Layers:
	-	`sha256:3330278a99c6d8715d2e22bde8ea5f89f5f5fb95534ac52e45424a8fab73c1fd`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d7465fe0a62b25696717b40ffb7aed5e4e5942145b573f0fc1cc612f8b11c`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d893ded57f82bb14cfe8258a8b49cf221e7e4b7581cc468f41564ebafa8017fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227906178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3bfc161a3c10708fc3e08c76b6ea7b7a3086212cbe8a2881593dab49b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:42 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39676fe8009672ced14ffa7e0d527ebdcfcd9909c02afbc97204fce62c41b77c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bca3b1a4681080d56d50fed1bc9ecc03c7eba0fb5558ce3533a8236ed1fc0c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8816a4545c8dd7279d6bd4d074560ce2b6769a3f98f8793d59ab322bd160ce4d`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 5.8 MB (5793597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab8f2de72f76a5f06196be92502620b578a4d358abcf93c5001b9ed3f32c1f`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79772aa74f1eae8ab8161d412141da67c1f7e7aaa398bcc9ae5043a4d596baf`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34007679fce091d3203b832c87b8f4c3d1c2809de5d7434c9d4036fd9bf98c`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 48.8 MB (48779936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e64b1ca3afd709e94aeec39594758aa1dd05e3f0a35b8e7dd7f33b93257d0a5`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae051ab9e6ff361121ac03f3b7391251e50a23033d5b50103609665abb866517`  
		Last Modified: Fri, 13 Mar 2026 23:12:53 GMT  
		Size: 126.7 MB (126685350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee96801673cf73a413bd74e781dac7f1729460f1a22c425d589ebf58a4f5d02`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0a95555d23e2e68e0faa2325a2f8ee25e2e48d492e4e72a8d2bf669f0574`  
		Last Modified: Fri, 13 Mar 2026 23:12:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8c75b94498a1631870b6bd71639f085345a27e2640b764ad37dab15472c7f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e042e80ea3c659632dd81daf530d619cd3f64035d18e128c206019653b50d`

```dockerfile
```

-	Layers:
	-	`sha256:81fda180811778da47155c0eb93e4a7ee7a6387191a312311e09e4b31285017e`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb736ecc0aa188c4abee2c00270f9ad0979736078c07637257a7abce00ef3fc`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45`

```console
$ docker pull mysql@sha256:0f34c70018dcbde655ba3eaba3d33c02198d392b9364974462eee13a903af385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45` - linux; amd64

```console
$ docker pull mysql@sha256:e778ad05466b7b12d6cbd13467271eb5ddad447bb676f79f9d1ab56572bb3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232285671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be417a60070a28d3b5e1db55800e358dcb8102083e2d587151fa58d98e785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:11:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:11:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd727943cf78a9f0ad1b104f4428b176dbb0279a5b1e92089efeb876948241`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183dada878863ad480368d0146eef3f2a4a01333f0ebd79c92116d5706977ca4`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca475193795ea762124043003f042cc6a5c2669294f0634add4d91f3e448d702`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 6.2 MB (6171304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a6efc32c61af1ae1fe48c1f8ea3ff872c21ce735ca8275edcc5255215f94a`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf107c1a2b33832ab078177d32f4b73961548ef7ce317b7ce7f0031e0db02193`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc630d3abcacff776255b4dfc25973c9af312598c15a6e3b43f17ab5261527`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 49.9 MB (49918946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b8625e4a373abd821788926da90e75cdaf2fc3a074a1b6587ef55834e8a6`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1297c1feceb7dd03edce7bb869223443cb6bf4517b8373c26a3bd6bb9bde9de`  
		Last Modified: Fri, 13 Mar 2026 23:13:19 GMT  
		Size: 128.1 MB (128098070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177fa0193b5c264d9f965d7bbedb4b16519340b616023ab19e6919986508781b`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122248aa49cd9e45c67433da6a74d9f8a81f317a6ede6a90092273b5a58e182`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:faade5acdd2acf4671ec95417e06ccc5ee4916d908080eded8c67b04e6b0b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51fa88745b7012cae4447bc76c389af4474dd79b2579d4ba8c50ad76feb700`

```dockerfile
```

-	Layers:
	-	`sha256:3330278a99c6d8715d2e22bde8ea5f89f5f5fb95534ac52e45424a8fab73c1fd`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d7465fe0a62b25696717b40ffb7aed5e4e5942145b573f0fc1cc612f8b11c`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d893ded57f82bb14cfe8258a8b49cf221e7e4b7581cc468f41564ebafa8017fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227906178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3bfc161a3c10708fc3e08c76b6ea7b7a3086212cbe8a2881593dab49b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:42 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39676fe8009672ced14ffa7e0d527ebdcfcd9909c02afbc97204fce62c41b77c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bca3b1a4681080d56d50fed1bc9ecc03c7eba0fb5558ce3533a8236ed1fc0c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8816a4545c8dd7279d6bd4d074560ce2b6769a3f98f8793d59ab322bd160ce4d`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 5.8 MB (5793597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab8f2de72f76a5f06196be92502620b578a4d358abcf93c5001b9ed3f32c1f`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79772aa74f1eae8ab8161d412141da67c1f7e7aaa398bcc9ae5043a4d596baf`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34007679fce091d3203b832c87b8f4c3d1c2809de5d7434c9d4036fd9bf98c`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 48.8 MB (48779936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e64b1ca3afd709e94aeec39594758aa1dd05e3f0a35b8e7dd7f33b93257d0a5`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae051ab9e6ff361121ac03f3b7391251e50a23033d5b50103609665abb866517`  
		Last Modified: Fri, 13 Mar 2026 23:12:53 GMT  
		Size: 126.7 MB (126685350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee96801673cf73a413bd74e781dac7f1729460f1a22c425d589ebf58a4f5d02`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0a95555d23e2e68e0faa2325a2f8ee25e2e48d492e4e72a8d2bf669f0574`  
		Last Modified: Fri, 13 Mar 2026 23:12:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45` - unknown; unknown

```console
$ docker pull mysql@sha256:8c75b94498a1631870b6bd71639f085345a27e2640b764ad37dab15472c7f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e042e80ea3c659632dd81daf530d619cd3f64035d18e128c206019653b50d`

```dockerfile
```

-	Layers:
	-	`sha256:81fda180811778da47155c0eb93e4a7ee7a6387191a312311e09e4b31285017e`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb736ecc0aa188c4abee2c00270f9ad0979736078c07637257a7abce00ef3fc`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-bookworm`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-debian`

```console
$ docker pull mysql@sha256:e90eaf1db3a7032d0dd1ea78141014f173eaeba62229a96124228df653e2db96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.45-debian` - linux; amd64

```console
$ docker pull mysql@sha256:9563a2f64eaa2cdc9164de2d2a76ddafce4356a9d6d534aeb8044e5dcd640326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183464741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34aa3e7f83cc1b63f2697c5bd89c2248b808d9d5373a5d4f3a72dee2d3a61163`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:42:27 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Mon, 16 Mar 2026 22:42:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
ENV GOSU_VERSION=1.19
# Mon, 16 Mar 2026 22:42:38 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Mon, 16 Mar 2026 22:42:38 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 16 Mar 2026 22:42:43 GMT
ENV MYSQL_VERSION=8.0.45-1debian12
# Mon, 16 Mar 2026 22:42:43 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
VOLUME [/var/lib/mysql]
# Mon, 16 Mar 2026 22:42:53 GMT
COPY config/ /etc/mysql/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Mon, 16 Mar 2026 22:42:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:42:53 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Mon, 16 Mar 2026 22:42:53 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e68e614f27fbb413a176db837874d771751afcca8680518b8b9502afc5f3f85`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4916b47a0e84df19644fae91a15098b6634fac737a2dc6ff4c4bc10158a51c`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.4 MB (4423383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4383ad717a22e9868a341a2c105ec87a1d0aada2aabe3cbddfd05c8b708823a7`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 1.2 MB (1248711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4c7e0f678dbdd1a352ce271395789d5c64b8f0bca208afb450ace5cbdf366`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dc241f96e4f4237388308240a0d3532a480cbfae6db486e06a933d88f37a85`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 15.3 MB (15295787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c830c5b026eb8004c0bad07fdee10cee28b6830bf597310870b56ca3b63b2af7`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 3.0 KB (3048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:064364b837bd9a375eea0c15eee508aee14fed141e2c3c47ba9583f319afa26d`  
		Last Modified: Mon, 16 Mar 2026 22:43:16 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8463ceca1d5fa880b50531fcc0da99b699a7e9a471e594667c112ae7fa1a05e9`  
		Last Modified: Mon, 16 Mar 2026 22:43:20 GMT  
		Size: 134.2 MB (134249828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791ac8f78e4c19796261b22605a397c62e77b481173d0dfc5d07306c58bb23b`  
		Last Modified: Mon, 16 Mar 2026 22:43:17 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5de9a02a13f92300fb3cf22b4b9a4e16de2e84f81bfb4ecd80088d9ef58c1d`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321c51e8c3ade48a41e496c8f1b13ed64d59cd6a6a1ad38db7609e842822481`  
		Last Modified: Mon, 16 Mar 2026 22:43:18 GMT  
		Size: 120.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ce17c4970b9a0db908872dbb4dd7fec01974861cacbcff376697fbd01e808e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4197758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e37d0628bc4f7ccd8343a70287b871e61b6201d3ee59eb7bbdb348292bb1de`

```dockerfile
```

-	Layers:
	-	`sha256:18b2e975dbe39eeb41189cd49942890d85eb20e7c55f4a0c47340703a5f69d9d`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 4.2 MB (4163505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1686dab13c765d69e9f26a96e606e8b28b93dc64a6a65ad23ff6fd3f221f65bb`  
		Last Modified: Mon, 16 Mar 2026 22:43:15 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oracle`

```console
$ docker pull mysql@sha256:0f34c70018dcbde655ba3eaba3d33c02198d392b9364974462eee13a903af385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e778ad05466b7b12d6cbd13467271eb5ddad447bb676f79f9d1ab56572bb3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232285671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be417a60070a28d3b5e1db55800e358dcb8102083e2d587151fa58d98e785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:11:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:11:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd727943cf78a9f0ad1b104f4428b176dbb0279a5b1e92089efeb876948241`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183dada878863ad480368d0146eef3f2a4a01333f0ebd79c92116d5706977ca4`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca475193795ea762124043003f042cc6a5c2669294f0634add4d91f3e448d702`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 6.2 MB (6171304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a6efc32c61af1ae1fe48c1f8ea3ff872c21ce735ca8275edcc5255215f94a`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf107c1a2b33832ab078177d32f4b73961548ef7ce317b7ce7f0031e0db02193`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc630d3abcacff776255b4dfc25973c9af312598c15a6e3b43f17ab5261527`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 49.9 MB (49918946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b8625e4a373abd821788926da90e75cdaf2fc3a074a1b6587ef55834e8a6`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1297c1feceb7dd03edce7bb869223443cb6bf4517b8373c26a3bd6bb9bde9de`  
		Last Modified: Fri, 13 Mar 2026 23:13:19 GMT  
		Size: 128.1 MB (128098070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177fa0193b5c264d9f965d7bbedb4b16519340b616023ab19e6919986508781b`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122248aa49cd9e45c67433da6a74d9f8a81f317a6ede6a90092273b5a58e182`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:faade5acdd2acf4671ec95417e06ccc5ee4916d908080eded8c67b04e6b0b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51fa88745b7012cae4447bc76c389af4474dd79b2579d4ba8c50ad76feb700`

```dockerfile
```

-	Layers:
	-	`sha256:3330278a99c6d8715d2e22bde8ea5f89f5f5fb95534ac52e45424a8fab73c1fd`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d7465fe0a62b25696717b40ffb7aed5e4e5942145b573f0fc1cc612f8b11c`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d893ded57f82bb14cfe8258a8b49cf221e7e4b7581cc468f41564ebafa8017fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227906178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3bfc161a3c10708fc3e08c76b6ea7b7a3086212cbe8a2881593dab49b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:42 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39676fe8009672ced14ffa7e0d527ebdcfcd9909c02afbc97204fce62c41b77c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bca3b1a4681080d56d50fed1bc9ecc03c7eba0fb5558ce3533a8236ed1fc0c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8816a4545c8dd7279d6bd4d074560ce2b6769a3f98f8793d59ab322bd160ce4d`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 5.8 MB (5793597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab8f2de72f76a5f06196be92502620b578a4d358abcf93c5001b9ed3f32c1f`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79772aa74f1eae8ab8161d412141da67c1f7e7aaa398bcc9ae5043a4d596baf`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34007679fce091d3203b832c87b8f4c3d1c2809de5d7434c9d4036fd9bf98c`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 48.8 MB (48779936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e64b1ca3afd709e94aeec39594758aa1dd05e3f0a35b8e7dd7f33b93257d0a5`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae051ab9e6ff361121ac03f3b7391251e50a23033d5b50103609665abb866517`  
		Last Modified: Fri, 13 Mar 2026 23:12:53 GMT  
		Size: 126.7 MB (126685350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee96801673cf73a413bd74e781dac7f1729460f1a22c425d589ebf58a4f5d02`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0a95555d23e2e68e0faa2325a2f8ee25e2e48d492e4e72a8d2bf669f0574`  
		Last Modified: Fri, 13 Mar 2026 23:12:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:8c75b94498a1631870b6bd71639f085345a27e2640b764ad37dab15472c7f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e042e80ea3c659632dd81daf530d619cd3f64035d18e128c206019653b50d`

```dockerfile
```

-	Layers:
	-	`sha256:81fda180811778da47155c0eb93e4a7ee7a6387191a312311e09e4b31285017e`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb736ecc0aa188c4abee2c00270f9ad0979736078c07637257a7abce00ef3fc`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.45-oraclelinux9`

```console
$ docker pull mysql@sha256:0f34c70018dcbde655ba3eaba3d33c02198d392b9364974462eee13a903af385
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.45-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e778ad05466b7b12d6cbd13467271eb5ddad447bb676f79f9d1ab56572bb3428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.3 MB (232285671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4be417a60070a28d3b5e1db55800e358dcb8102083e2d587151fa58d98e785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:11:15 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:11:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:40 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:44 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:44 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:45 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:45 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd727943cf78a9f0ad1b104f4428b176dbb0279a5b1e92089efeb876948241`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183dada878863ad480368d0146eef3f2a4a01333f0ebd79c92116d5706977ca4`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca475193795ea762124043003f042cc6a5c2669294f0634add4d91f3e448d702`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 6.2 MB (6171304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a6efc32c61af1ae1fe48c1f8ea3ff872c21ce735ca8275edcc5255215f94a`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf107c1a2b33832ab078177d32f4b73961548ef7ce317b7ce7f0031e0db02193`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fcc630d3abcacff776255b4dfc25973c9af312598c15a6e3b43f17ab5261527`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 49.9 MB (49918946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575b8625e4a373abd821788926da90e75cdaf2fc3a074a1b6587ef55834e8a6`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1297c1feceb7dd03edce7bb869223443cb6bf4517b8373c26a3bd6bb9bde9de`  
		Last Modified: Fri, 13 Mar 2026 23:13:19 GMT  
		Size: 128.1 MB (128098070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177fa0193b5c264d9f965d7bbedb4b16519340b616023ab19e6919986508781b`  
		Last Modified: Fri, 13 Mar 2026 23:13:16 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122248aa49cd9e45c67433da6a74d9f8a81f317a6ede6a90092273b5a58e182`  
		Last Modified: Fri, 13 Mar 2026 23:13:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:faade5acdd2acf4671ec95417e06ccc5ee4916d908080eded8c67b04e6b0b1ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14992436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e51fa88745b7012cae4447bc76c389af4474dd79b2579d4ba8c50ad76feb700`

```dockerfile
```

-	Layers:
	-	`sha256:3330278a99c6d8715d2e22bde8ea5f89f5f5fb95534ac52e45424a8fab73c1fd`  
		Last Modified: Fri, 13 Mar 2026 23:13:15 GMT  
		Size: 15.0 MB (14957525 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:096d7465fe0a62b25696717b40ffb7aed5e4e5942145b573f0fc1cc612f8b11c`  
		Last Modified: Fri, 13 Mar 2026 23:13:14 GMT  
		Size: 34.9 KB (34911 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.45-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d893ded57f82bb14cfe8258a8b49cf221e7e4b7581cc468f41564ebafa8017fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227906178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fa3bfc161a3c10708fc3e08c76b6ea7b7a3086212cbe8a2881593dab49b984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:42 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:42 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_MAJOR=8.0
# Fri, 13 Mar 2026 23:11:10 GMT
ENV MYSQL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:11:11 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:41 GMT
ENV MYSQL_SHELL_VERSION=8.0.45-1.el9
# Fri, 13 Mar 2026 23:12:19 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Fri, 13 Mar 2026 23:12:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:19 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:19 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39676fe8009672ced14ffa7e0d527ebdcfcd9909c02afbc97204fce62c41b77c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bca3b1a4681080d56d50fed1bc9ecc03c7eba0fb5558ce3533a8236ed1fc0c`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8816a4545c8dd7279d6bd4d074560ce2b6769a3f98f8793d59ab322bd160ce4d`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 5.8 MB (5793597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63ab8f2de72f76a5f06196be92502620b578a4d358abcf93c5001b9ed3f32c1f`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 2.6 KB (2603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79772aa74f1eae8ab8161d412141da67c1f7e7aaa398bcc9ae5043a4d596baf`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba34007679fce091d3203b832c87b8f4c3d1c2809de5d7434c9d4036fd9bf98c`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 48.8 MB (48779936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e64b1ca3afd709e94aeec39594758aa1dd05e3f0a35b8e7dd7f33b93257d0a5`  
		Last Modified: Fri, 13 Mar 2026 23:12:50 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae051ab9e6ff361121ac03f3b7391251e50a23033d5b50103609665abb866517`  
		Last Modified: Fri, 13 Mar 2026 23:12:53 GMT  
		Size: 126.7 MB (126685350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee96801673cf73a413bd74e781dac7f1729460f1a22c425d589ebf58a4f5d02`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0a95555d23e2e68e0faa2325a2f8ee25e2e48d492e4e72a8d2bf669f0574`  
		Last Modified: Fri, 13 Mar 2026 23:12:52 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.45-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:8c75b94498a1631870b6bd71639f085345a27e2640b764ad37dab15472c7f135
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14991032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60e042e80ea3c659632dd81daf530d619cd3f64035d18e128c206019653b50d`

```dockerfile
```

-	Layers:
	-	`sha256:81fda180811778da47155c0eb93e4a7ee7a6387191a312311e09e4b31285017e`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 15.0 MB (14955873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdb736ecc0aa188c4abee2c00270f9ad0979736078c07637257a7abce00ef3fc`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 35.2 KB (35159 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oracle`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.8-oraclelinux9`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oracle`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6-oraclelinux9`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oracle`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.6.0-oraclelinux9`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.6.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.6.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.6.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:be18eb9dc45eea9b86cb74f8c68ab92ce8569ecc37ea4e6fade02e37036c5ff4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:f7f7f7861832e484abb52031b086c2820b28a8a7dc182ee4b3a32de993de3b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.2 MB (233210028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ffa1ed2ee9eb2e5268d59419446f1bbeb4b47983a65540f18cc097587969f2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:47 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:49 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:49 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:12 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:13 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:10 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:10 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:10 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9839a1557aa83abb7b81097bdd02dc4550d33c0ed5aecfa757724e1808473f3d`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f224d94174ec43e7377dfb238267aec82d23632ec2243cc7cdf2bd5345316ce5`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 783.6 KB (783557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76531228703a0958b3d7e27c84ecddcae94898e7e4f6109040ab04795f68b787`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 6.2 MB (6171351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e79a5d7e37c1e19c36db33773d02d25c5f9f4171c769ee215b29e3aade85c5cc`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6f1f8035236f7c4b5763dc9f55318875158426bb07c86b04b10674f5aaa4b9`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432b203620bced3ddb389a82f3d5702991fcd32e028fa4b2c95d104056ade753`  
		Last Modified: Fri, 13 Mar 2026 23:12:42 GMT  
		Size: 47.8 MB (47810211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8a4aec6c64aa7fb42a38b644f4ae7808fcd32cd6944335c655b49259319a494`  
		Last Modified: Fri, 13 Mar 2026 23:12:44 GMT  
		Size: 131.1 MB (131131231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8644b9d847378f91da1c8443ed72fe5cca6ab38f578ce770da73fa8269273b7`  
		Last Modified: Fri, 13 Mar 2026 23:12:41 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:934e24cf812cdfaa5270df4c877116ee67759691876eb4d688678b12f98d0387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15268552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca944d1ea8e389abaf281d6ca01c903427b188a8559aaffbb70401946e258ef`

```dockerfile
```

-	Layers:
	-	`sha256:7b689e56014156d32522756234ac0f6b70621b194cca48d3b6ab47e0cbe00e23`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 15.2 MB (15234346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94f46c72f9e8dfe50a50bcd66c4e1a2791ca60b0adc7558bf6828cfbcf6852e6`  
		Last Modified: Fri, 13 Mar 2026 23:12:39 GMT  
		Size: 34.2 KB (34206 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9a94718d7520441b6855caccb46198c48885c6ad8c81d22c5f15b0d687e42a0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228689103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb9f139f381b9bebc40ffe985aa506b008c3178963ca41b2fcbc22de7856c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:40 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:40 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_MAJOR=8.4
# Fri, 13 Mar 2026 23:11:09 GMT
ENV MYSQL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:11:09 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:38 GMT
ENV MYSQL_SHELL_VERSION=8.4.8-1.el9
# Fri, 13 Mar 2026 23:12:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:12:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:12:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:12:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:12:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a87bbaabeb846a11e6a32b2cc74e024bd4737c19d50fb5c22cee939c1d004`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395ed09572ca0e9c30443cc916d0a4950dd2b96aab483425f7bca32cf4879525`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 737.5 KB (737526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0c16a609941077d6832aabe64328db7ef3fd81233b139fdcbc85ca8bf0beab`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 5.8 MB (5793582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87705f0a19162730536577972b5c3671c4c7208ad5de1d801fbe5e4a29460103`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2af7cc285a658ffa560a3cc9903e19973c26c1261ddd21e704e6b550a9022a`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8c57a1e4d621454cc401f3ab8149f116320a89425ed535fed0ea0ee2bd148`  
		Last Modified: Fri, 13 Mar 2026 23:12:49 GMT  
		Size: 46.7 MB (46700806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e004d6d0d098baad0a245489ca8ae54ba0d68d42832decee8492ee31d23bb`  
		Last Modified: Fri, 13 Mar 2026 23:12:40 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f140e4e85b4592f111bf319d3cc1d5cc40c437e512fe641e76a971cffa6163a`  
		Last Modified: Fri, 13 Mar 2026 23:12:51 GMT  
		Size: 129.5 MB (129547528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a657146b5ab89169a17c12579946783b9ceac38020f1a3fb11083721ed45dc0d`  
		Last Modified: Fri, 13 Mar 2026 23:12:48 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:e2f3310808ce70980796a29215d0d9ac607060700824cd5a04127b020fcc8aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15267278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43c07f6ea5a09cc55a950c70e703c831571d9c9117d8d176762e122e66aea56`

```dockerfile
```

-	Layers:
	-	`sha256:c75f1a9f60b8df3d53d6d13d187e194b185e4060d26db23a28b8fc5e953e7d24`  
		Last Modified: Fri, 13 Mar 2026 23:12:47 GMT  
		Size: 15.2 MB (15232766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:875a13310b0430f4b52877ab4e9ab3636d052ffa993dcd999b4d3470837feee5`  
		Last Modified: Fri, 13 Mar 2026 23:12:46 GMT  
		Size: 34.5 KB (34512 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:c1667ed4366709204bdf4514c7d979dfdbc29af43f9840def436b039eefc5f88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:54ea66dae32f9c08069b505b1d0b4bd3814ab91de9a30a005cc6808915754d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.3 MB (266347266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4d012ac036a1b1185f073570b53c073e11eb3dce801ce8f13569d92be366bf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:12:04 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:12:04 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:10:09 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:10:11 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:10:11 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:38 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:39 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:39 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:11:08 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:49 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:49 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:49 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:df11b1bcbaee7bc8a76e5b2867de05fee4f9e3e48339461adc6794666b1d52ca`  
		Last Modified: Fri, 13 Mar 2026 22:12:15 GMT  
		Size: 47.3 MB (47304210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d0d4e183c69de847603a1b1dff7b47f85da450e68fbf3ca75474b0ce17db0e`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d58e86e20ab38e5e77f9fcf4b791a84fc71c3d3fd18637b0a65768a032a27`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 783.6 KB (783556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73a8a0cdd3528731928ded76f5b4f36f744e86bfbc3a44e64b2b78b3bd2281c`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 6.2 MB (6171291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdf47a0b3c9190e6587bd6f6c3726ce576c0c1c4b04056cecf407facd2b40538`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ecd6491b857c0f35d9792e997251168262791008cfd66a0ca38b7958c7eeac`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e5f11992e5f6d2c4d261989cb0899fd0850d2a5d5fdd69379411aba945a652`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 51.4 MB (51447567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ab040157e6c18539e45de5715aefaaf9e2d0740f607feacf1e67373800323`  
		Last Modified: Fri, 13 Mar 2026 23:12:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb02db9d051cef95b6879079d6740b75e582a1f648bc85e51036906adbff53e`  
		Last Modified: Fri, 13 Mar 2026 23:12:30 GMT  
		Size: 160.6 MB (160631155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e94ccf4f6d7311fa5f5fd4e997c0188d9c9b2df1a1191fa64992bd2318c56f3`  
		Last Modified: Fri, 13 Mar 2026 23:12:27 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:aff90e5beae0c50486f75bd39bb7b6bb02b7805da863f59b1ba3bfd1aba27365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16332711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7defcf236243948fa0afe6def352c24b848eac8491ce3a8d9a631d74c5e5357b`

```dockerfile
```

-	Layers:
	-	`sha256:299fede5ea7f8ca23d1d872432d3a73b0556d75f7a8966827c23aefeba72970a`  
		Last Modified: Fri, 13 Mar 2026 23:12:25 GMT  
		Size: 16.3 MB (16297436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:829c5e9f227cf70d019147b71c21a2e40236a76ce84d68e96f5537dd511584d8`  
		Last Modified: Fri, 13 Mar 2026 23:12:24 GMT  
		Size: 35.3 KB (35275 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:ed73bffb124e523980f2f05f97efb613a52a9d4f3987d2ab5e8e8202b08042ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261469825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36cb056a351cfeece5a39befcba40ad70d8623697440068775d9aa6275ad31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 13 Mar 2026 22:11:21 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 13 Mar 2026 22:11:21 GMT
CMD ["/bin/bash"]
# Fri, 13 Mar 2026 23:09:43 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Fri, 13 Mar 2026 23:09:45 GMT
ENV GOSU_VERSION=1.19
# Fri, 13 Mar 2026 23:09:45 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Fri, 13 Mar 2026 23:10:13 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_MAJOR=innovation
# Fri, 13 Mar 2026 23:10:14 GMT
ENV MYSQL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:10:14 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Fri, 13 Mar 2026 23:10:43 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Fri, 13 Mar 2026 23:10:44 GMT
ENV MYSQL_SHELL_VERSION=9.6.0-1.el9
# Fri, 13 Mar 2026 23:11:27 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Fri, 13 Mar 2026 23:11:27 GMT
VOLUME [/var/lib/mysql]
# Fri, 13 Mar 2026 23:11:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 23:11:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 13 Mar 2026 23:11:28 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Fri, 13 Mar 2026 23:11:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b877fed8ea0c89aa9f3a89457df18f21650f64f87c1a34f66ced9c394634b85e`  
		Last Modified: Fri, 13 Mar 2026 22:11:32 GMT  
		Size: 45.9 MB (45900186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ce986ba86c4cd5a896dc232cb9081b64b2d7a9c811746a20bc60bebcaa742f`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388de34e30dfc5b202ed167bffd2e7c1fc29c1a7a74be0812ef3189067cc32f2`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 737.5 KB (737522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144255d2d499514c737e748eeb4144ed57bf3f4d3284a26cf49e3fd143d9d6df`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 5.8 MB (5793630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52c415828f9b62df56cde6f4f359aced35bb3ce7ca4ab74a17c960a0b10c848`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c607a0c43901cb8795007d36b0b3f1ad31f3b2456bd8c0843a3fedb5cec877a`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daae71ebd5166877672e1cd1dd9c76cd0cf65e0ecd13e77b603e1d8fb32a0b92`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 50.1 MB (50088318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce621bbaaa95b2241477a38f7372114cc5110fc325ed314e7ee9258913cb77a7`  
		Last Modified: Fri, 13 Mar 2026 23:12:04 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125392532eece4d34e5017c3be6e535f73e0d623ad5bdf6fadd5f00c1d0d07f`  
		Last Modified: Fri, 13 Mar 2026 23:12:07 GMT  
		Size: 158.9 MB (158940684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2ba10371fc43d55f0b91613cc476522be45ef7189dac685a2ff96ae42ab13d`  
		Last Modified: Fri, 13 Mar 2026 23:12:05 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:963fa7715947ecbf307b316aae05e6462b14915709a3fb09a2b00b0161f240b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16331507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85c497cb07cd524e777a882ba695da7de662230d2cb677fc1782e534e401418f`

```dockerfile
```

-	Layers:
	-	`sha256:52fb8d490411a702a96b105ddd155e78fa36c86f6b90dfd3e648c2b42061c3ce`  
		Last Modified: Fri, 13 Mar 2026 23:12:03 GMT  
		Size: 16.3 MB (16295892 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed91ba832c7b9b5d70bb23efeb25692cd039bce470bfbc4afc5a71783f2c785`  
		Last Modified: Fri, 13 Mar 2026 23:12:02 GMT  
		Size: 35.6 KB (35615 bytes)  
		MIME: application/vnd.in-toto+json
