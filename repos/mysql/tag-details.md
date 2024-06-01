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
-	[`mysql:8.0.37`](#mysql8037)
-	[`mysql:8.0.37-bookworm`](#mysql8037-bookworm)
-	[`mysql:8.0.37-debian`](#mysql8037-debian)
-	[`mysql:8.0.37-oracle`](#mysql8037-oracle)
-	[`mysql:8.0.37-oraclelinux9`](#mysql8037-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.0`](#mysql840)
-	[`mysql:8.4.0-oracle`](#mysql840-oracle)
-	[`mysql:8.4.0-oraclelinux9`](#mysql840-oraclelinux9)
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
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:56ac33f0ad10a07829f6635afe8c0728b2c3456418595c512962f42400ff6ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:274eac608b1582955cea35f8d0c9af84326d192282686bd26dde43424bc82197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba4c9bcaa80ab33bfb308aa4e951f6b9cb9b4462e068718154b3691cf706d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2546f0005eefe884144789a413dabe0b19473f4387e4deee26f4d56d5e6b13d1`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb57662dd7fe2f638e90aa4cbb246d4fb1222c281368b956f17df6296eaa8a0`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 6.7 MB (6711506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14d8034cde87f80239a4852668aa5fe846b1e3b3a98dfbe12015a380e1b1f`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73124c42ecbec3c571c85dceab85f51a4e42f644ff5897cc027f790d3b6eef3a`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74830c23cea021d995dc16f7354dc2528577e9231ee1a4622683bea0088fe306`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 49.1 MB (49147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0139fa28450536f5b37f71d0f80ff4b2eb78e83ce93086da650edd7f38a07fee`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165942f42d603cb22e693919466754b99859f6f6e006ab9bfa61c753be687b4`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 60.2 MB (60171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915d634a34439adcb83735dd8bd9e114b8b497f19f39294147161f74007925a`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f1e1ee309c4bca23f035e310c4e81b093233d1d5be5bea5078f8317b56090`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:060b11c439831b533677d5cdd487f6913b9f8b0b59a46fb32a8364a385e0dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b461614fef7d152c702720468766f1021129a47ee3eaafc4f71c76ea8aa09`

```dockerfile
```

-	Layers:
	-	`sha256:f4c42e958147206280e53052d18a3fe48282b0998eb15bf39b836a459d26069b`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277eac1124677973519a65b9ce11b324a267fe892d108b5c58858c922953728`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d6eab4bb20a5384d37c43965926de1a4f0b85222e4ee343cfcbe76e120804cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece306faea624bf93d444fcc8ef264718e6bd430304bb497403b49d3f4735d0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8f50b4ce6f804f449897b82462340514534d9a30edd558dfcedfc1220c758`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26e70af83de12238e384e17012258a04aa5df7eaa099eabfc318c543f5b03`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 48.0 MB (48031042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795c0f20a3dd39907aeaff5f35dd57e713e78151e8e232203000f7ebc72f4ac`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fe6e72d4e78f3609010c11e9c441dcff40a36f7cef9d4480b3705d325d8a8`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 67.6 MB (67648647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902ff9733a922d5924af3fb1d2d9baff32823ea2491e2856281eb12596cb19b`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3fcf3b9c3db1640574ff55aaf77848b6ca8d2991f197168af898c6b5302f`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:00ee225458c36bff44d465a8ae70ff7e53fc6b6e021f438ee362d6aea2fc93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd578fe23cc3b069ce1e38231077dc6201cfcfd56257b817fff1a5976ef678fc`

```dockerfile
```

-	Layers:
	-	`sha256:23d87f3dbdf175c0f660a2a1c5927273df5cca5a88daa7955f9240a4e7fd8b7b`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 13.4 MB (13444112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df17f7ec9010422a0baabaa049f98adb0c0c961ed5d00030b49f97d3560f793`  
		Last Modified: Thu, 09 May 2024 23:40:28 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:1579fe3a97a436cc10824fc771a07fcedc92213e7ab7604eb5d2976ca419abc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:d255f59008e43c69924f94ab33126d102b77eb745aac888eaf3bd5c48ccc6640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24a8f68bd7a14aa12e5afa8717986b0ea5f92baf3d08659875897214c34d753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Apr 2024 04:15:13 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029cd480822ba5424d84ef7f0b05f2156ba949f0ae6185c2ecd78b1f5f0f794e`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225aa208e69abcea3b0b05ebbabb408b0756b9459832a8aa1cd09ab4a48d3de4`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.4 MB (4422737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239b7cd9357f790a4a9f9c417e9b4176b1ee82e8a9294b160d58100729682f6`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.4 MB (1449160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ff6da3549f4ce186a700b962de00177204f60e9658276358643dcf7f3e2a7`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae062e186090a72b17830eda821b901c7134bee48a62db2ce7bd36ca2a0f6b6c`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 15.3 MB (15281663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040a0a6075c4990db79e238b8001a0498197cb233131527a26927c19e249492b`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe50e9a549947d107fc1cdbfe7388bd66172c31a1ffaf9dd7a47f50bc79f079`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e648b481d7aaf4ac5ee72fcd57de119d0c47aef8c7c1b9d29c7246df9a1fd1`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 134.4 MB (134409360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8839099acf6fb098bfbcb3e703a2813be8ec3b99b96f0002496ea3f4ff267b7`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3c8c905986d0b613cb8c0f2129cbcd113d8891ec5dd4210351001a9c4f109`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13925c5104b8976de6028931a06838fc20f4177ba22fdc23264e8206036ef322`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:bcb0dd990b779aa59bc0ba9810231827c003c992e6c8c16ff31d5fdb5de20121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707467742f190f2266278f608d7ddbf23fb0b9b526d5f18860148c4c34c760`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa8ecc05731e36397f8a4c9d065d910e984edc6724a2a54a16325724b05d57`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc780c8a0f0ec055bb5c08e5fb9b0e53b6ff6b31ceaa9af4c25217ff706009eb`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:1579fe3a97a436cc10824fc771a07fcedc92213e7ab7604eb5d2976ca419abc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:d255f59008e43c69924f94ab33126d102b77eb745aac888eaf3bd5c48ccc6640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24a8f68bd7a14aa12e5afa8717986b0ea5f92baf3d08659875897214c34d753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Apr 2024 04:15:13 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029cd480822ba5424d84ef7f0b05f2156ba949f0ae6185c2ecd78b1f5f0f794e`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225aa208e69abcea3b0b05ebbabb408b0756b9459832a8aa1cd09ab4a48d3de4`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.4 MB (4422737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239b7cd9357f790a4a9f9c417e9b4176b1ee82e8a9294b160d58100729682f6`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.4 MB (1449160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ff6da3549f4ce186a700b962de00177204f60e9658276358643dcf7f3e2a7`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae062e186090a72b17830eda821b901c7134bee48a62db2ce7bd36ca2a0f6b6c`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 15.3 MB (15281663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040a0a6075c4990db79e238b8001a0498197cb233131527a26927c19e249492b`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe50e9a549947d107fc1cdbfe7388bd66172c31a1ffaf9dd7a47f50bc79f079`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e648b481d7aaf4ac5ee72fcd57de119d0c47aef8c7c1b9d29c7246df9a1fd1`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 134.4 MB (134409360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8839099acf6fb098bfbcb3e703a2813be8ec3b99b96f0002496ea3f4ff267b7`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3c8c905986d0b613cb8c0f2129cbcd113d8891ec5dd4210351001a9c4f109`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13925c5104b8976de6028931a06838fc20f4177ba22fdc23264e8206036ef322`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:bcb0dd990b779aa59bc0ba9810231827c003c992e6c8c16ff31d5fdb5de20121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707467742f190f2266278f608d7ddbf23fb0b9b526d5f18860148c4c34c760`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa8ecc05731e36397f8a4c9d065d910e984edc6724a2a54a16325724b05d57`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc780c8a0f0ec055bb5c08e5fb9b0e53b6ff6b31ceaa9af4c25217ff706009eb`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:56ac33f0ad10a07829f6635afe8c0728b2c3456418595c512962f42400ff6ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:274eac608b1582955cea35f8d0c9af84326d192282686bd26dde43424bc82197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba4c9bcaa80ab33bfb308aa4e951f6b9cb9b4462e068718154b3691cf706d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2546f0005eefe884144789a413dabe0b19473f4387e4deee26f4d56d5e6b13d1`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb57662dd7fe2f638e90aa4cbb246d4fb1222c281368b956f17df6296eaa8a0`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 6.7 MB (6711506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14d8034cde87f80239a4852668aa5fe846b1e3b3a98dfbe12015a380e1b1f`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73124c42ecbec3c571c85dceab85f51a4e42f644ff5897cc027f790d3b6eef3a`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74830c23cea021d995dc16f7354dc2528577e9231ee1a4622683bea0088fe306`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 49.1 MB (49147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0139fa28450536f5b37f71d0f80ff4b2eb78e83ce93086da650edd7f38a07fee`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165942f42d603cb22e693919466754b99859f6f6e006ab9bfa61c753be687b4`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 60.2 MB (60171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915d634a34439adcb83735dd8bd9e114b8b497f19f39294147161f74007925a`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f1e1ee309c4bca23f035e310c4e81b093233d1d5be5bea5078f8317b56090`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:060b11c439831b533677d5cdd487f6913b9f8b0b59a46fb32a8364a385e0dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b461614fef7d152c702720468766f1021129a47ee3eaafc4f71c76ea8aa09`

```dockerfile
```

-	Layers:
	-	`sha256:f4c42e958147206280e53052d18a3fe48282b0998eb15bf39b836a459d26069b`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277eac1124677973519a65b9ce11b324a267fe892d108b5c58858c922953728`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d6eab4bb20a5384d37c43965926de1a4f0b85222e4ee343cfcbe76e120804cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece306faea624bf93d444fcc8ef264718e6bd430304bb497403b49d3f4735d0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8f50b4ce6f804f449897b82462340514534d9a30edd558dfcedfc1220c758`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26e70af83de12238e384e17012258a04aa5df7eaa099eabfc318c543f5b03`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 48.0 MB (48031042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795c0f20a3dd39907aeaff5f35dd57e713e78151e8e232203000f7ebc72f4ac`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fe6e72d4e78f3609010c11e9c441dcff40a36f7cef9d4480b3705d325d8a8`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 67.6 MB (67648647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902ff9733a922d5924af3fb1d2d9baff32823ea2491e2856281eb12596cb19b`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3fcf3b9c3db1640574ff55aaf77848b6ca8d2991f197168af898c6b5302f`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:00ee225458c36bff44d465a8ae70ff7e53fc6b6e021f438ee362d6aea2fc93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd578fe23cc3b069ce1e38231077dc6201cfcfd56257b817fff1a5976ef678fc`

```dockerfile
```

-	Layers:
	-	`sha256:23d87f3dbdf175c0f660a2a1c5927273df5cca5a88daa7955f9240a4e7fd8b7b`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 13.4 MB (13444112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df17f7ec9010422a0baabaa049f98adb0c0c961ed5d00030b49f97d3560f793`  
		Last Modified: Thu, 09 May 2024 23:40:28 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:56ac33f0ad10a07829f6635afe8c0728b2c3456418595c512962f42400ff6ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:274eac608b1582955cea35f8d0c9af84326d192282686bd26dde43424bc82197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba4c9bcaa80ab33bfb308aa4e951f6b9cb9b4462e068718154b3691cf706d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2546f0005eefe884144789a413dabe0b19473f4387e4deee26f4d56d5e6b13d1`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb57662dd7fe2f638e90aa4cbb246d4fb1222c281368b956f17df6296eaa8a0`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 6.7 MB (6711506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14d8034cde87f80239a4852668aa5fe846b1e3b3a98dfbe12015a380e1b1f`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73124c42ecbec3c571c85dceab85f51a4e42f644ff5897cc027f790d3b6eef3a`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74830c23cea021d995dc16f7354dc2528577e9231ee1a4622683bea0088fe306`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 49.1 MB (49147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0139fa28450536f5b37f71d0f80ff4b2eb78e83ce93086da650edd7f38a07fee`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165942f42d603cb22e693919466754b99859f6f6e006ab9bfa61c753be687b4`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 60.2 MB (60171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915d634a34439adcb83735dd8bd9e114b8b497f19f39294147161f74007925a`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f1e1ee309c4bca23f035e310c4e81b093233d1d5be5bea5078f8317b56090`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:060b11c439831b533677d5cdd487f6913b9f8b0b59a46fb32a8364a385e0dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b461614fef7d152c702720468766f1021129a47ee3eaafc4f71c76ea8aa09`

```dockerfile
```

-	Layers:
	-	`sha256:f4c42e958147206280e53052d18a3fe48282b0998eb15bf39b836a459d26069b`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277eac1124677973519a65b9ce11b324a267fe892d108b5c58858c922953728`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d6eab4bb20a5384d37c43965926de1a4f0b85222e4ee343cfcbe76e120804cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece306faea624bf93d444fcc8ef264718e6bd430304bb497403b49d3f4735d0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8f50b4ce6f804f449897b82462340514534d9a30edd558dfcedfc1220c758`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26e70af83de12238e384e17012258a04aa5df7eaa099eabfc318c543f5b03`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 48.0 MB (48031042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795c0f20a3dd39907aeaff5f35dd57e713e78151e8e232203000f7ebc72f4ac`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fe6e72d4e78f3609010c11e9c441dcff40a36f7cef9d4480b3705d325d8a8`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 67.6 MB (67648647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902ff9733a922d5924af3fb1d2d9baff32823ea2491e2856281eb12596cb19b`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3fcf3b9c3db1640574ff55aaf77848b6ca8d2991f197168af898c6b5302f`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:00ee225458c36bff44d465a8ae70ff7e53fc6b6e021f438ee362d6aea2fc93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd578fe23cc3b069ce1e38231077dc6201cfcfd56257b817fff1a5976ef678fc`

```dockerfile
```

-	Layers:
	-	`sha256:23d87f3dbdf175c0f660a2a1c5927273df5cca5a88daa7955f9240a4e7fd8b7b`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 13.4 MB (13444112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df17f7ec9010422a0baabaa049f98adb0c0c961ed5d00030b49f97d3560f793`  
		Last Modified: Thu, 09 May 2024 23:40:28 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37`

```console
$ docker pull mysql@sha256:56ac33f0ad10a07829f6635afe8c0728b2c3456418595c512962f42400ff6ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37` - linux; amd64

```console
$ docker pull mysql@sha256:274eac608b1582955cea35f8d0c9af84326d192282686bd26dde43424bc82197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba4c9bcaa80ab33bfb308aa4e951f6b9cb9b4462e068718154b3691cf706d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2546f0005eefe884144789a413dabe0b19473f4387e4deee26f4d56d5e6b13d1`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb57662dd7fe2f638e90aa4cbb246d4fb1222c281368b956f17df6296eaa8a0`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 6.7 MB (6711506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14d8034cde87f80239a4852668aa5fe846b1e3b3a98dfbe12015a380e1b1f`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73124c42ecbec3c571c85dceab85f51a4e42f644ff5897cc027f790d3b6eef3a`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74830c23cea021d995dc16f7354dc2528577e9231ee1a4622683bea0088fe306`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 49.1 MB (49147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0139fa28450536f5b37f71d0f80ff4b2eb78e83ce93086da650edd7f38a07fee`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165942f42d603cb22e693919466754b99859f6f6e006ab9bfa61c753be687b4`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 60.2 MB (60171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915d634a34439adcb83735dd8bd9e114b8b497f19f39294147161f74007925a`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f1e1ee309c4bca23f035e310c4e81b093233d1d5be5bea5078f8317b56090`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:060b11c439831b533677d5cdd487f6913b9f8b0b59a46fb32a8364a385e0dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b461614fef7d152c702720468766f1021129a47ee3eaafc4f71c76ea8aa09`

```dockerfile
```

-	Layers:
	-	`sha256:f4c42e958147206280e53052d18a3fe48282b0998eb15bf39b836a459d26069b`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277eac1124677973519a65b9ce11b324a267fe892d108b5c58858c922953728`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d6eab4bb20a5384d37c43965926de1a4f0b85222e4ee343cfcbe76e120804cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece306faea624bf93d444fcc8ef264718e6bd430304bb497403b49d3f4735d0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8f50b4ce6f804f449897b82462340514534d9a30edd558dfcedfc1220c758`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26e70af83de12238e384e17012258a04aa5df7eaa099eabfc318c543f5b03`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 48.0 MB (48031042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795c0f20a3dd39907aeaff5f35dd57e713e78151e8e232203000f7ebc72f4ac`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fe6e72d4e78f3609010c11e9c441dcff40a36f7cef9d4480b3705d325d8a8`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 67.6 MB (67648647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902ff9733a922d5924af3fb1d2d9baff32823ea2491e2856281eb12596cb19b`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3fcf3b9c3db1640574ff55aaf77848b6ca8d2991f197168af898c6b5302f`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37` - unknown; unknown

```console
$ docker pull mysql@sha256:00ee225458c36bff44d465a8ae70ff7e53fc6b6e021f438ee362d6aea2fc93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd578fe23cc3b069ce1e38231077dc6201cfcfd56257b817fff1a5976ef678fc`

```dockerfile
```

-	Layers:
	-	`sha256:23d87f3dbdf175c0f660a2a1c5927273df5cca5a88daa7955f9240a4e7fd8b7b`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 13.4 MB (13444112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df17f7ec9010422a0baabaa049f98adb0c0c961ed5d00030b49f97d3560f793`  
		Last Modified: Thu, 09 May 2024 23:40:28 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-bookworm`

```console
$ docker pull mysql@sha256:1579fe3a97a436cc10824fc771a07fcedc92213e7ab7604eb5d2976ca419abc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:d255f59008e43c69924f94ab33126d102b77eb745aac888eaf3bd5c48ccc6640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24a8f68bd7a14aa12e5afa8717986b0ea5f92baf3d08659875897214c34d753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Apr 2024 04:15:13 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029cd480822ba5424d84ef7f0b05f2156ba949f0ae6185c2ecd78b1f5f0f794e`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225aa208e69abcea3b0b05ebbabb408b0756b9459832a8aa1cd09ab4a48d3de4`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.4 MB (4422737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239b7cd9357f790a4a9f9c417e9b4176b1ee82e8a9294b160d58100729682f6`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.4 MB (1449160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ff6da3549f4ce186a700b962de00177204f60e9658276358643dcf7f3e2a7`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae062e186090a72b17830eda821b901c7134bee48a62db2ce7bd36ca2a0f6b6c`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 15.3 MB (15281663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040a0a6075c4990db79e238b8001a0498197cb233131527a26927c19e249492b`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe50e9a549947d107fc1cdbfe7388bd66172c31a1ffaf9dd7a47f50bc79f079`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e648b481d7aaf4ac5ee72fcd57de119d0c47aef8c7c1b9d29c7246df9a1fd1`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 134.4 MB (134409360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8839099acf6fb098bfbcb3e703a2813be8ec3b99b96f0002496ea3f4ff267b7`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3c8c905986d0b613cb8c0f2129cbcd113d8891ec5dd4210351001a9c4f109`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13925c5104b8976de6028931a06838fc20f4177ba22fdc23264e8206036ef322`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:bcb0dd990b779aa59bc0ba9810231827c003c992e6c8c16ff31d5fdb5de20121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707467742f190f2266278f608d7ddbf23fb0b9b526d5f18860148c4c34c760`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa8ecc05731e36397f8a4c9d065d910e984edc6724a2a54a16325724b05d57`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc780c8a0f0ec055bb5c08e5fb9b0e53b6ff6b31ceaa9af4c25217ff706009eb`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-debian`

```console
$ docker pull mysql@sha256:1579fe3a97a436cc10824fc771a07fcedc92213e7ab7604eb5d2976ca419abc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.37-debian` - linux; amd64

```console
$ docker pull mysql@sha256:d255f59008e43c69924f94ab33126d102b77eb745aac888eaf3bd5c48ccc6640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184723442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24a8f68bd7a14aa12e5afa8717986b0ea5f92baf3d08659875897214c34d753`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 30 Apr 2024 04:15:13 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["bash"]
# Tue, 30 Apr 2024 04:15:13 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV GOSU_VERSION=1.17
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 30 Apr 2024 04:15:13 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 30 Apr 2024 04:15:13 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
VOLUME [/var/lib/mysql]
# Tue, 30 Apr 2024 04:15:13 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 30 Apr 2024 04:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 30 Apr 2024 04:15:13 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 30 Apr 2024 04:15:13 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029cd480822ba5424d84ef7f0b05f2156ba949f0ae6185c2ecd78b1f5f0f794e`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225aa208e69abcea3b0b05ebbabb408b0756b9459832a8aa1cd09ab4a48d3de4`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.4 MB (4422737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d239b7cd9357f790a4a9f9c417e9b4176b1ee82e8a9294b160d58100729682f6`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 1.4 MB (1449160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0ff6da3549f4ce186a700b962de00177204f60e9658276358643dcf7f3e2a7`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae062e186090a72b17830eda821b901c7134bee48a62db2ce7bd36ca2a0f6b6c`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 15.3 MB (15281663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040a0a6075c4990db79e238b8001a0498197cb233131527a26927c19e249492b`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 2.5 KB (2502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe50e9a549947d107fc1cdbfe7388bd66172c31a1ffaf9dd7a47f50bc79f079`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e648b481d7aaf4ac5ee72fcd57de119d0c47aef8c7c1b9d29c7246df9a1fd1`  
		Last Modified: Tue, 14 May 2024 02:56:38 GMT  
		Size: 134.4 MB (134409360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8839099acf6fb098bfbcb3e703a2813be8ec3b99b96f0002496ea3f4ff267b7`  
		Last Modified: Tue, 14 May 2024 02:56:36 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e3c8c905986d0b613cb8c0f2129cbcd113d8891ec5dd4210351001a9c4f109`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 5.2 KB (5172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13925c5104b8976de6028931a06838fc20f4177ba22fdc23264e8206036ef322`  
		Last Modified: Tue, 14 May 2024 02:56:37 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:bcb0dd990b779aa59bc0ba9810231827c003c992e6c8c16ff31d5fdb5de20121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22707467742f190f2266278f608d7ddbf23fb0b9b526d5f18860148c4c34c760`

```dockerfile
```

-	Layers:
	-	`sha256:ceaa8ecc05731e36397f8a4c9d065d910e984edc6724a2a54a16325724b05d57`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 4.0 MB (3953561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc780c8a0f0ec055bb5c08e5fb9b0e53b6ff6b31ceaa9af4c25217ff706009eb`  
		Last Modified: Tue, 14 May 2024 02:56:35 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oracle`

```console
$ docker pull mysql@sha256:56ac33f0ad10a07829f6635afe8c0728b2c3456418595c512962f42400ff6ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:274eac608b1582955cea35f8d0c9af84326d192282686bd26dde43424bc82197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba4c9bcaa80ab33bfb308aa4e951f6b9cb9b4462e068718154b3691cf706d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2546f0005eefe884144789a413dabe0b19473f4387e4deee26f4d56d5e6b13d1`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb57662dd7fe2f638e90aa4cbb246d4fb1222c281368b956f17df6296eaa8a0`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 6.7 MB (6711506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14d8034cde87f80239a4852668aa5fe846b1e3b3a98dfbe12015a380e1b1f`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73124c42ecbec3c571c85dceab85f51a4e42f644ff5897cc027f790d3b6eef3a`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74830c23cea021d995dc16f7354dc2528577e9231ee1a4622683bea0088fe306`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 49.1 MB (49147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0139fa28450536f5b37f71d0f80ff4b2eb78e83ce93086da650edd7f38a07fee`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165942f42d603cb22e693919466754b99859f6f6e006ab9bfa61c753be687b4`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 60.2 MB (60171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915d634a34439adcb83735dd8bd9e114b8b497f19f39294147161f74007925a`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f1e1ee309c4bca23f035e310c4e81b093233d1d5be5bea5078f8317b56090`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:060b11c439831b533677d5cdd487f6913b9f8b0b59a46fb32a8364a385e0dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b461614fef7d152c702720468766f1021129a47ee3eaafc4f71c76ea8aa09`

```dockerfile
```

-	Layers:
	-	`sha256:f4c42e958147206280e53052d18a3fe48282b0998eb15bf39b836a459d26069b`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277eac1124677973519a65b9ce11b324a267fe892d108b5c58858c922953728`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d6eab4bb20a5384d37c43965926de1a4f0b85222e4ee343cfcbe76e120804cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece306faea624bf93d444fcc8ef264718e6bd430304bb497403b49d3f4735d0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8f50b4ce6f804f449897b82462340514534d9a30edd558dfcedfc1220c758`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26e70af83de12238e384e17012258a04aa5df7eaa099eabfc318c543f5b03`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 48.0 MB (48031042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795c0f20a3dd39907aeaff5f35dd57e713e78151e8e232203000f7ebc72f4ac`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fe6e72d4e78f3609010c11e9c441dcff40a36f7cef9d4480b3705d325d8a8`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 67.6 MB (67648647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902ff9733a922d5924af3fb1d2d9baff32823ea2491e2856281eb12596cb19b`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3fcf3b9c3db1640574ff55aaf77848b6ca8d2991f197168af898c6b5302f`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:00ee225458c36bff44d465a8ae70ff7e53fc6b6e021f438ee362d6aea2fc93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd578fe23cc3b069ce1e38231077dc6201cfcfd56257b817fff1a5976ef678fc`

```dockerfile
```

-	Layers:
	-	`sha256:23d87f3dbdf175c0f660a2a1c5927273df5cca5a88daa7955f9240a4e7fd8b7b`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 13.4 MB (13444112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df17f7ec9010422a0baabaa049f98adb0c0c961ed5d00030b49f97d3560f793`  
		Last Modified: Thu, 09 May 2024 23:40:28 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.37-oraclelinux9`

```console
$ docker pull mysql@sha256:56ac33f0ad10a07829f6635afe8c0728b2c3456418595c512962f42400ff6ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.37-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:274eac608b1582955cea35f8d0c9af84326d192282686bd26dde43424bc82197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eba4c9bcaa80ab33bfb308aa4e951f6b9cb9b4462e068718154b3691cf706d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2546f0005eefe884144789a413dabe0b19473f4387e4deee26f4d56d5e6b13d1`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb57662dd7fe2f638e90aa4cbb246d4fb1222c281368b956f17df6296eaa8a0`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 6.7 MB (6711506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb14d8034cde87f80239a4852668aa5fe846b1e3b3a98dfbe12015a380e1b1f`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73124c42ecbec3c571c85dceab85f51a4e42f644ff5897cc027f790d3b6eef3a`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74830c23cea021d995dc16f7354dc2528577e9231ee1a4622683bea0088fe306`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 49.1 MB (49147386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0139fa28450536f5b37f71d0f80ff4b2eb78e83ce93086da650edd7f38a07fee`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5165942f42d603cb22e693919466754b99859f6f6e006ab9bfa61c753be687b4`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 60.2 MB (60171019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2915d634a34439adcb83735dd8bd9e114b8b497f19f39294147161f74007925a`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1f1e1ee309c4bca23f035e310c4e81b093233d1d5be5bea5078f8317b56090`  
		Last Modified: Sat, 01 Jun 2024 01:50:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:060b11c439831b533677d5cdd487f6913b9f8b0b59a46fb32a8364a385e0dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56b461614fef7d152c702720468766f1021129a47ee3eaafc4f71c76ea8aa09`

```dockerfile
```

-	Layers:
	-	`sha256:f4c42e958147206280e53052d18a3fe48282b0998eb15bf39b836a459d26069b`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 13.4 MB (13448981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e277eac1124677973519a65b9ce11b324a267fe892d108b5c58858c922953728`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 34.7 KB (34731 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.37-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:d6eab4bb20a5384d37c43965926de1a4f0b85222e4ee343cfcbe76e120804cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece306faea624bf93d444fcc8ef264718e6bd430304bb497403b49d3f4735d0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.0
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa8f50b4ce6f804f449897b82462340514534d9a30edd558dfcedfc1220c758`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f26e70af83de12238e384e17012258a04aa5df7eaa099eabfc318c543f5b03`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 48.0 MB (48031042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7795c0f20a3dd39907aeaff5f35dd57e713e78151e8e232203000f7ebc72f4ac`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841fe6e72d4e78f3609010c11e9c441dcff40a36f7cef9d4480b3705d325d8a8`  
		Last Modified: Thu, 09 May 2024 23:40:31 GMT  
		Size: 67.6 MB (67648647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a902ff9733a922d5924af3fb1d2d9baff32823ea2491e2856281eb12596cb19b`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 5.2 KB (5180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6c3fcf3b9c3db1640574ff55aaf77848b6ca8d2991f197168af898c6b5302f`  
		Last Modified: Thu, 09 May 2024 23:40:30 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.37-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:00ee225458c36bff44d465a8ae70ff7e53fc6b6e021f438ee362d6aea2fc93cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13478858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd578fe23cc3b069ce1e38231077dc6201cfcfd56257b817fff1a5976ef678fc`

```dockerfile
```

-	Layers:
	-	`sha256:23d87f3dbdf175c0f660a2a1c5927273df5cca5a88daa7955f9240a4e7fd8b7b`  
		Last Modified: Thu, 09 May 2024 23:40:29 GMT  
		Size: 13.4 MB (13444112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6df17f7ec9010422a0baabaa049f98adb0c0c961ed5d00030b49f97d3560f793`  
		Last Modified: Thu, 09 May 2024 23:40:28 GMT  
		Size: 34.7 KB (34746 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oracle`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.0-oraclelinux9`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:378a84fd304ad01952cd9275dd88f116ccd675cf2b60a082d7f3a9589fe14c0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:d4990507327f4d08aaf57d9c7e2e0250260e9f6ef7fa0e0bfe822c37ad2e1b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168700380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd86ff8ce8c2d30f02607e184cbfd73eb581e22a451e4a1847a102318bc2926`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:aa0e8a24fb10efad12d0ad144ad3590843c14a46d9621c490269079b0e68826d in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:07bc88e18c4aea4343fc16a9930da57308d4df45d3d234aebcd5b1c1833ee290`  
		Last Modified: Sat, 01 Jun 2024 00:49:58 GMT  
		Size: 49.0 MB (48994878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9c1668bf493c4df11d8a9377aeb8ef94c277c39d700470d6757f4affe812fa`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021dda8eecff015672845c8c131d475eccb83c09569a18640c2cda4399decf2`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 983.0 KB (983004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb61b56acac1145d05c716918b447019808fac364743d1232e647845748f5020`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 6.7 MB (6711529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bca83908a5b1425517e978c51f3b8631610670037c49db9c3663a7915e20c53`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165e8b3d37ca389e737cbc06dbd776556f3fb96311ed68ea52825fbc64685450`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1b086f129564f4f57b1cf79b288cf54a9e5c3a1c43219db46a1b493d40cded`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 47.2 MB (47215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6516684849c81829a8787e5e56a203bad4854df16430fa2e3ca837d94e1d4`  
		Last Modified: Sat, 01 Jun 2024 01:50:28 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed90f5355e12edb07b8cdaa438ef1d088e2e3121ed5b04904aaf98e79555c572`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 64.8 MB (64786544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0412f59ab2b5360b2f2648828b0e7dd7483aa35d13a6623fcc7752d23414e9ea`  
		Last Modified: Sat, 01 Jun 2024 01:50:29 GMT  
		Size: 5.2 KB (5185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:fc88aa38fce5a0c3be54d4cfd0dda9c351854c5d28285509baedf4f322f7d755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb72e2ef7c20b35c5072fcb35d6e883a53438280073b1d0725ee26e54002755`

```dockerfile
```

-	Layers:
	-	`sha256:90bc47518ea9636409ddf1e628a6a9294beb6da6b862efbe17ea68f59607cb94`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 13.6 MB (13560850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:093735f4437645cfae494cafd8547dbac018e3ca4906a65553d91d0c09285aa5`  
		Last Modified: Sat, 01 Jun 2024 01:50:27 GMT  
		Size: 35.9 KB (35876 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:79bf3d05d420c85d21702dcde491ec36be535c79200cc83f1298dd838a6f1dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165936004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7c9c15d9ea6c54c2b01a6711d3dae4412f67eb89d27509ca857e592f23929d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Wed, 01 May 2024 07:22:24 GMT
ADD file:d92cdce307b01a5d65a1de97ab4359302d32346aac991d1d547486f6bad75cb3 in / 
# Wed, 01 May 2024 07:22:24 GMT
CMD ["/bin/bash"]
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV GOSU_VERSION=1.17
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_MAJOR=8.4
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Wed, 01 May 2024 07:22:24 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Wed, 01 May 2024 07:22:24 GMT
VOLUME [/var/lib/mysql]
# Wed, 01 May 2024 07:22:24 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 01 May 2024 07:22:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 May 2024 07:22:24 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Wed, 01 May 2024 07:22:24 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:3c4da62cd991f18afd4514c4ea7300378d2cbe34ca3392e4136c1e28b59f15ba`  
		Last Modified: Thu, 09 May 2024 22:07:36 GMT  
		Size: 47.7 MB (47653800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6246d8c92d7fdd7ccda103fff5418e73900ae7d681af888a49ad238c564e677f`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e7eb4221427f63ba631c9d4418617d016709e4ff742d3539066a5f0c2bfb95`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f787785dc51829259a1a029295b8427fe3326c03f36f80f4e1023232b5ecb800`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 6.3 MB (6313952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7585e10db184ab64d8aae49167c81e44358cccf58fb680af4a20f640791ae1d5`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c69999011c03fe9caa79c25b4cc5b668950bf164c0529da1cd5a707b2230b546`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1142f05d9006da74f47862396c0649055f72490479abcff23198e262e143f3d5`  
		Last Modified: Thu, 09 May 2024 23:39:18 GMT  
		Size: 46.1 MB (46084546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d598a5053b5cad951d8eaaedaebfdbc5463a880de8c075a48f7c2e5eae7c08d3`  
		Last Modified: Thu, 09 May 2024 23:39:16 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de4462059cc5c84ea3164bd0179dc65734627f2a496a0c56a1002054ee36aab`  
		Last Modified: Thu, 09 May 2024 23:39:19 GMT  
		Size: 65.0 MB (64960942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca92666741087fc28d7590e97b73f8c452955effa4f061f16451c05ba0934a3`  
		Last Modified: Thu, 09 May 2024 23:39:17 GMT  
		Size: 5.2 KB (5176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ad0644d4ea4c2291a9c3990d2e0373112058f7e7d8a3da4865c0c079b9c878cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13590170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db833d8a95d398a7d7abb7248afc9a264d2df8542ff5040708dec1968ca905c`

```dockerfile
```

-	Layers:
	-	`sha256:f10b193dff936fdc257b9489b413aa675fa6d6268749f4398581f7bd61a68873`  
		Last Modified: Thu, 09 May 2024 23:39:15 GMT  
		Size: 13.6 MB (13555047 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4f13cdab2d2ed579bf08f115518bdcf6b9957b97ef28e61a960a5077aa6431`  
		Last Modified: Thu, 09 May 2024 23:39:14 GMT  
		Size: 35.1 KB (35123 bytes)  
		MIME: application/vnd.in-toto+json
