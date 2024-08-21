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
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:ec5625b52f8c71b11021f4be1f5bec67fb5b2671602b636e67c17251f589f213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:9a8447808e3833090d76bf92c04fc44f9b779066d14ace41f968e395c9e52a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c620843cab4e76831182bb1670738b35200bf6a7ea0e622c787012f4099890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa6458eab97bc76b4ae0ef225cefcb51dc0884686664dd7d00850eab5eb90a`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a4e01dc1c4aa6b31c606eb9c9f0fcbcca240015235e1ea8d2ab4344ae9e4d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbdbd530386c203aa33aaaaf02583909244f80690dc9978a2273d1851a3a18`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 6.7 MB (6711406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca25b4b52499df95f4fad0908feccca5563d0ff8331e7103495c51e10bf17dd`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16ab611cbbe1b5e06cf5a2a327b6ede6b514e64428cf475bc47dc75ec1d779`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69135a274f66b9cf23adacfb7ddf3bbf88612b1e867140cf26a8447b72ed284`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 49.2 MB (49160558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e40bace318d5fade3d3ccbd703930aae32bdccff4badcbd9afae755c6698e1`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf65b590e0aef3e0bd73638df71f14aad0e763148322bca5de19f79d4793c`  
		Last Modified: Wed, 21 Aug 2024 01:06:44 GMT  
		Size: 60.9 MB (60912934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c6fba2c9ff62ea90bd5ecc9ad66d35c86663042cc2a522fec22c7c8bb21de`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dd3f5a0fd4263387738f5c33cb5173d65b9fc4bdd78ea385cd4314767f5f`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:bea5510d65a01f5369d960f2f372757ba69e24a7ffc323ea02b0023748803023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea691b471ef06aac118a35ddfc6560049ba384d73560e6406f4a8bdd211bb622`

```dockerfile
```

-	Layers:
	-	`sha256:39c5d05eaca8ea8561ba9cce32a8440224c1ed4f0f2dae9e72daa772e31aeb0d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 13.7 MB (13706929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f5282c85f0d22aa279bc34ef1e238896ba94eac669f24c08ec2badcb73a751`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1ca09a74711bc63b9740bf4208442f19b024b2db3398cd7fa71a81a6cc92d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171321422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe32947929a8eeba712a80603e11503d767b9eb450c327c6d592f5703ee912f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc48526a281bd364b3d5d26d3054277fee60a88fd32b25c9e3f6a65a8315672`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366025c7c632c67b05f1970b08b0eb0af9c4fed296768f8f872a1cab355f20b`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 48.0 MB (48034746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8297d9b1017584a1ed1d547033948998a0a28f03f5a9173e0ea135b6bbee9`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f301a28857c255522a9e0e7013f4897ef440921b8bac17dec30463ed15fa5`  
		Last Modified: Wed, 21 Aug 2024 01:10:40 GMT  
		Size: 68.4 MB (68395162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2854b9042eef691d8718cc4a8b0016956bac1bb7a83c475cf0d90b046b0e0f`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2491bb6c634a56c59c46ce1274bcbc5f030fdf579bb6b5384cae30f9e280a38f`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:d24c490c9fab9c5a9726e76c08fdb4fb995a8c917f364ce318a79944d44784d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e97f022ae52727ea62e22fabc19635398527c7fa53b4e93a252a678742f7691`

```dockerfile
```

-	Layers:
	-	`sha256:f01ac659fcd2ea85efb2b9896d465464ba03996eceb1b0c0fb6fd5873926d9d1`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 13.7 MB (13702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b10068afd288b7e7d37498071a10670e0113e78926909b2cb54ef23e4bc37`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
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
$ docker pull mysql@sha256:ec5625b52f8c71b11021f4be1f5bec67fb5b2671602b636e67c17251f589f213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9a8447808e3833090d76bf92c04fc44f9b779066d14ace41f968e395c9e52a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c620843cab4e76831182bb1670738b35200bf6a7ea0e622c787012f4099890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa6458eab97bc76b4ae0ef225cefcb51dc0884686664dd7d00850eab5eb90a`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a4e01dc1c4aa6b31c606eb9c9f0fcbcca240015235e1ea8d2ab4344ae9e4d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbdbd530386c203aa33aaaaf02583909244f80690dc9978a2273d1851a3a18`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 6.7 MB (6711406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca25b4b52499df95f4fad0908feccca5563d0ff8331e7103495c51e10bf17dd`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16ab611cbbe1b5e06cf5a2a327b6ede6b514e64428cf475bc47dc75ec1d779`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69135a274f66b9cf23adacfb7ddf3bbf88612b1e867140cf26a8447b72ed284`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 49.2 MB (49160558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e40bace318d5fade3d3ccbd703930aae32bdccff4badcbd9afae755c6698e1`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf65b590e0aef3e0bd73638df71f14aad0e763148322bca5de19f79d4793c`  
		Last Modified: Wed, 21 Aug 2024 01:06:44 GMT  
		Size: 60.9 MB (60912934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c6fba2c9ff62ea90bd5ecc9ad66d35c86663042cc2a522fec22c7c8bb21de`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dd3f5a0fd4263387738f5c33cb5173d65b9fc4bdd78ea385cd4314767f5f`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bea5510d65a01f5369d960f2f372757ba69e24a7ffc323ea02b0023748803023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea691b471ef06aac118a35ddfc6560049ba384d73560e6406f4a8bdd211bb622`

```dockerfile
```

-	Layers:
	-	`sha256:39c5d05eaca8ea8561ba9cce32a8440224c1ed4f0f2dae9e72daa772e31aeb0d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 13.7 MB (13706929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f5282c85f0d22aa279bc34ef1e238896ba94eac669f24c08ec2badcb73a751`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1ca09a74711bc63b9740bf4208442f19b024b2db3398cd7fa71a81a6cc92d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171321422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe32947929a8eeba712a80603e11503d767b9eb450c327c6d592f5703ee912f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc48526a281bd364b3d5d26d3054277fee60a88fd32b25c9e3f6a65a8315672`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366025c7c632c67b05f1970b08b0eb0af9c4fed296768f8f872a1cab355f20b`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 48.0 MB (48034746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8297d9b1017584a1ed1d547033948998a0a28f03f5a9173e0ea135b6bbee9`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f301a28857c255522a9e0e7013f4897ef440921b8bac17dec30463ed15fa5`  
		Last Modified: Wed, 21 Aug 2024 01:10:40 GMT  
		Size: 68.4 MB (68395162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2854b9042eef691d8718cc4a8b0016956bac1bb7a83c475cf0d90b046b0e0f`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2491bb6c634a56c59c46ce1274bcbc5f030fdf579bb6b5384cae30f9e280a38f`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d24c490c9fab9c5a9726e76c08fdb4fb995a8c917f364ce318a79944d44784d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e97f022ae52727ea62e22fabc19635398527c7fa53b4e93a252a678742f7691`

```dockerfile
```

-	Layers:
	-	`sha256:f01ac659fcd2ea85efb2b9896d465464ba03996eceb1b0c0fb6fd5873926d9d1`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 13.7 MB (13702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b10068afd288b7e7d37498071a10670e0113e78926909b2cb54ef23e4bc37`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:ec5625b52f8c71b11021f4be1f5bec67fb5b2671602b636e67c17251f589f213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9a8447808e3833090d76bf92c04fc44f9b779066d14ace41f968e395c9e52a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c620843cab4e76831182bb1670738b35200bf6a7ea0e622c787012f4099890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa6458eab97bc76b4ae0ef225cefcb51dc0884686664dd7d00850eab5eb90a`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a4e01dc1c4aa6b31c606eb9c9f0fcbcca240015235e1ea8d2ab4344ae9e4d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbdbd530386c203aa33aaaaf02583909244f80690dc9978a2273d1851a3a18`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 6.7 MB (6711406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca25b4b52499df95f4fad0908feccca5563d0ff8331e7103495c51e10bf17dd`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16ab611cbbe1b5e06cf5a2a327b6ede6b514e64428cf475bc47dc75ec1d779`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69135a274f66b9cf23adacfb7ddf3bbf88612b1e867140cf26a8447b72ed284`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 49.2 MB (49160558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e40bace318d5fade3d3ccbd703930aae32bdccff4badcbd9afae755c6698e1`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf65b590e0aef3e0bd73638df71f14aad0e763148322bca5de19f79d4793c`  
		Last Modified: Wed, 21 Aug 2024 01:06:44 GMT  
		Size: 60.9 MB (60912934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c6fba2c9ff62ea90bd5ecc9ad66d35c86663042cc2a522fec22c7c8bb21de`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dd3f5a0fd4263387738f5c33cb5173d65b9fc4bdd78ea385cd4314767f5f`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bea5510d65a01f5369d960f2f372757ba69e24a7ffc323ea02b0023748803023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea691b471ef06aac118a35ddfc6560049ba384d73560e6406f4a8bdd211bb622`

```dockerfile
```

-	Layers:
	-	`sha256:39c5d05eaca8ea8561ba9cce32a8440224c1ed4f0f2dae9e72daa772e31aeb0d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 13.7 MB (13706929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f5282c85f0d22aa279bc34ef1e238896ba94eac669f24c08ec2badcb73a751`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1ca09a74711bc63b9740bf4208442f19b024b2db3398cd7fa71a81a6cc92d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171321422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe32947929a8eeba712a80603e11503d767b9eb450c327c6d592f5703ee912f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc48526a281bd364b3d5d26d3054277fee60a88fd32b25c9e3f6a65a8315672`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366025c7c632c67b05f1970b08b0eb0af9c4fed296768f8f872a1cab355f20b`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 48.0 MB (48034746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8297d9b1017584a1ed1d547033948998a0a28f03f5a9173e0ea135b6bbee9`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f301a28857c255522a9e0e7013f4897ef440921b8bac17dec30463ed15fa5`  
		Last Modified: Wed, 21 Aug 2024 01:10:40 GMT  
		Size: 68.4 MB (68395162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2854b9042eef691d8718cc4a8b0016956bac1bb7a83c475cf0d90b046b0e0f`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2491bb6c634a56c59c46ce1274bcbc5f030fdf579bb6b5384cae30f9e280a38f`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d24c490c9fab9c5a9726e76c08fdb4fb995a8c917f364ce318a79944d44784d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e97f022ae52727ea62e22fabc19635398527c7fa53b4e93a252a678742f7691`

```dockerfile
```

-	Layers:
	-	`sha256:f01ac659fcd2ea85efb2b9896d465464ba03996eceb1b0c0fb6fd5873926d9d1`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 13.7 MB (13702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b10068afd288b7e7d37498071a10670e0113e78926909b2cb54ef23e4bc37`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39`

```console
$ docker pull mysql@sha256:ec5625b52f8c71b11021f4be1f5bec67fb5b2671602b636e67c17251f589f213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.39` - linux; amd64

```console
$ docker pull mysql@sha256:9a8447808e3833090d76bf92c04fc44f9b779066d14ace41f968e395c9e52a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c620843cab4e76831182bb1670738b35200bf6a7ea0e622c787012f4099890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa6458eab97bc76b4ae0ef225cefcb51dc0884686664dd7d00850eab5eb90a`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a4e01dc1c4aa6b31c606eb9c9f0fcbcca240015235e1ea8d2ab4344ae9e4d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbdbd530386c203aa33aaaaf02583909244f80690dc9978a2273d1851a3a18`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 6.7 MB (6711406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca25b4b52499df95f4fad0908feccca5563d0ff8331e7103495c51e10bf17dd`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16ab611cbbe1b5e06cf5a2a327b6ede6b514e64428cf475bc47dc75ec1d779`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69135a274f66b9cf23adacfb7ddf3bbf88612b1e867140cf26a8447b72ed284`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 49.2 MB (49160558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e40bace318d5fade3d3ccbd703930aae32bdccff4badcbd9afae755c6698e1`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf65b590e0aef3e0bd73638df71f14aad0e763148322bca5de19f79d4793c`  
		Last Modified: Wed, 21 Aug 2024 01:06:44 GMT  
		Size: 60.9 MB (60912934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c6fba2c9ff62ea90bd5ecc9ad66d35c86663042cc2a522fec22c7c8bb21de`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dd3f5a0fd4263387738f5c33cb5173d65b9fc4bdd78ea385cd4314767f5f`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39` - unknown; unknown

```console
$ docker pull mysql@sha256:bea5510d65a01f5369d960f2f372757ba69e24a7ffc323ea02b0023748803023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea691b471ef06aac118a35ddfc6560049ba384d73560e6406f4a8bdd211bb622`

```dockerfile
```

-	Layers:
	-	`sha256:39c5d05eaca8ea8561ba9cce32a8440224c1ed4f0f2dae9e72daa772e31aeb0d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 13.7 MB (13706929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f5282c85f0d22aa279bc34ef1e238896ba94eac669f24c08ec2badcb73a751`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.39` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1ca09a74711bc63b9740bf4208442f19b024b2db3398cd7fa71a81a6cc92d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171321422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe32947929a8eeba712a80603e11503d767b9eb450c327c6d592f5703ee912f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc48526a281bd364b3d5d26d3054277fee60a88fd32b25c9e3f6a65a8315672`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366025c7c632c67b05f1970b08b0eb0af9c4fed296768f8f872a1cab355f20b`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 48.0 MB (48034746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8297d9b1017584a1ed1d547033948998a0a28f03f5a9173e0ea135b6bbee9`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f301a28857c255522a9e0e7013f4897ef440921b8bac17dec30463ed15fa5`  
		Last Modified: Wed, 21 Aug 2024 01:10:40 GMT  
		Size: 68.4 MB (68395162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2854b9042eef691d8718cc4a8b0016956bac1bb7a83c475cf0d90b046b0e0f`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2491bb6c634a56c59c46ce1274bcbc5f030fdf579bb6b5384cae30f9e280a38f`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39` - unknown; unknown

```console
$ docker pull mysql@sha256:d24c490c9fab9c5a9726e76c08fdb4fb995a8c917f364ce318a79944d44784d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e97f022ae52727ea62e22fabc19635398527c7fa53b4e93a252a678742f7691`

```dockerfile
```

-	Layers:
	-	`sha256:f01ac659fcd2ea85efb2b9896d465464ba03996eceb1b0c0fb6fd5873926d9d1`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 13.7 MB (13702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b10068afd288b7e7d37498071a10670e0113e78926909b2cb54ef23e4bc37`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
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
$ docker pull mysql@sha256:ec5625b52f8c71b11021f4be1f5bec67fb5b2671602b636e67c17251f589f213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.39-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9a8447808e3833090d76bf92c04fc44f9b779066d14ace41f968e395c9e52a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c620843cab4e76831182bb1670738b35200bf6a7ea0e622c787012f4099890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa6458eab97bc76b4ae0ef225cefcb51dc0884686664dd7d00850eab5eb90a`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a4e01dc1c4aa6b31c606eb9c9f0fcbcca240015235e1ea8d2ab4344ae9e4d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbdbd530386c203aa33aaaaf02583909244f80690dc9978a2273d1851a3a18`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 6.7 MB (6711406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca25b4b52499df95f4fad0908feccca5563d0ff8331e7103495c51e10bf17dd`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16ab611cbbe1b5e06cf5a2a327b6ede6b514e64428cf475bc47dc75ec1d779`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69135a274f66b9cf23adacfb7ddf3bbf88612b1e867140cf26a8447b72ed284`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 49.2 MB (49160558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e40bace318d5fade3d3ccbd703930aae32bdccff4badcbd9afae755c6698e1`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf65b590e0aef3e0bd73638df71f14aad0e763148322bca5de19f79d4793c`  
		Last Modified: Wed, 21 Aug 2024 01:06:44 GMT  
		Size: 60.9 MB (60912934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c6fba2c9ff62ea90bd5ecc9ad66d35c86663042cc2a522fec22c7c8bb21de`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dd3f5a0fd4263387738f5c33cb5173d65b9fc4bdd78ea385cd4314767f5f`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:bea5510d65a01f5369d960f2f372757ba69e24a7ffc323ea02b0023748803023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea691b471ef06aac118a35ddfc6560049ba384d73560e6406f4a8bdd211bb622`

```dockerfile
```

-	Layers:
	-	`sha256:39c5d05eaca8ea8561ba9cce32a8440224c1ed4f0f2dae9e72daa772e31aeb0d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 13.7 MB (13706929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f5282c85f0d22aa279bc34ef1e238896ba94eac669f24c08ec2badcb73a751`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.39-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1ca09a74711bc63b9740bf4208442f19b024b2db3398cd7fa71a81a6cc92d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171321422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe32947929a8eeba712a80603e11503d767b9eb450c327c6d592f5703ee912f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc48526a281bd364b3d5d26d3054277fee60a88fd32b25c9e3f6a65a8315672`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366025c7c632c67b05f1970b08b0eb0af9c4fed296768f8f872a1cab355f20b`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 48.0 MB (48034746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8297d9b1017584a1ed1d547033948998a0a28f03f5a9173e0ea135b6bbee9`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f301a28857c255522a9e0e7013f4897ef440921b8bac17dec30463ed15fa5`  
		Last Modified: Wed, 21 Aug 2024 01:10:40 GMT  
		Size: 68.4 MB (68395162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2854b9042eef691d8718cc4a8b0016956bac1bb7a83c475cf0d90b046b0e0f`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2491bb6c634a56c59c46ce1274bcbc5f030fdf579bb6b5384cae30f9e280a38f`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:d24c490c9fab9c5a9726e76c08fdb4fb995a8c917f364ce318a79944d44784d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e97f022ae52727ea62e22fabc19635398527c7fa53b4e93a252a678742f7691`

```dockerfile
```

-	Layers:
	-	`sha256:f01ac659fcd2ea85efb2b9896d465464ba03996eceb1b0c0fb6fd5873926d9d1`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 13.7 MB (13702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b10068afd288b7e7d37498071a10670e0113e78926909b2cb54ef23e4bc37`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-oraclelinux9`

```console
$ docker pull mysql@sha256:ec5625b52f8c71b11021f4be1f5bec67fb5b2671602b636e67c17251f589f213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.39-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9a8447808e3833090d76bf92c04fc44f9b779066d14ace41f968e395c9e52a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166772301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c620843cab4e76831182bb1670738b35200bf6a7ea0e622c787012f4099890`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fa6458eab97bc76b4ae0ef225cefcb51dc0884686664dd7d00850eab5eb90a`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d40a4e01dc1c4aa6b31c606eb9c9f0fcbcca240015235e1ea8d2ab4344ae9e4d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacbdbd530386c203aa33aaaaf02583909244f80690dc9978a2273d1851a3a18`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 6.7 MB (6711406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca25b4b52499df95f4fad0908feccca5563d0ff8331e7103495c51e10bf17dd`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 2.6 KB (2604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a16ab611cbbe1b5e06cf5a2a327b6ede6b514e64428cf475bc47dc75ec1d779`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69135a274f66b9cf23adacfb7ddf3bbf88612b1e867140cf26a8447b72ed284`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 49.2 MB (49160558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e40bace318d5fade3d3ccbd703930aae32bdccff4badcbd9afae755c6698e1`  
		Last Modified: Wed, 21 Aug 2024 01:06:42 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000cf65b590e0aef3e0bd73638df71f14aad0e763148322bca5de19f79d4793c`  
		Last Modified: Wed, 21 Aug 2024 01:06:44 GMT  
		Size: 60.9 MB (60912934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9c6fba2c9ff62ea90bd5ecc9ad66d35c86663042cc2a522fec22c7c8bb21de`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8127dd3f5a0fd4263387738f5c33cb5173d65b9fc4bdd78ea385cd4314767f5f`  
		Last Modified: Wed, 21 Aug 2024 01:06:43 GMT  
		Size: 119.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:bea5510d65a01f5369d960f2f372757ba69e24a7ffc323ea02b0023748803023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea691b471ef06aac118a35ddfc6560049ba384d73560e6406f4a8bdd211bb622`

```dockerfile
```

-	Layers:
	-	`sha256:39c5d05eaca8ea8561ba9cce32a8440224c1ed4f0f2dae9e72daa772e31aeb0d`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 13.7 MB (13706929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28f5282c85f0d22aa279bc34ef1e238896ba94eac669f24c08ec2badcb73a751`  
		Last Modified: Wed, 21 Aug 2024 01:06:41 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.39-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:1ca09a74711bc63b9740bf4208442f19b024b2db3398cd7fa71a81a6cc92d489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171321422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe32947929a8eeba712a80603e11503d767b9eb450c327c6d592f5703ee912f5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc48526a281bd364b3d5d26d3054277fee60a88fd32b25c9e3f6a65a8315672`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366025c7c632c67b05f1970b08b0eb0af9c4fed296768f8f872a1cab355f20b`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 48.0 MB (48034746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f8297d9b1017584a1ed1d547033948998a0a28f03f5a9173e0ea135b6bbee9`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1f301a28857c255522a9e0e7013f4897ef440921b8bac17dec30463ed15fa5`  
		Last Modified: Wed, 21 Aug 2024 01:10:40 GMT  
		Size: 68.4 MB (68395162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2854b9042eef691d8718cc4a8b0016956bac1bb7a83c475cf0d90b046b0e0f`  
		Last Modified: Wed, 21 Aug 2024 01:10:39 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2491bb6c634a56c59c46ce1274bcbc5f030fdf579bb6b5384cae30f9e280a38f`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:d24c490c9fab9c5a9726e76c08fdb4fb995a8c917f364ce318a79944d44784d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13737119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e97f022ae52727ea62e22fabc19635398527c7fa53b4e93a252a678742f7691`

```dockerfile
```

-	Layers:
	-	`sha256:f01ac659fcd2ea85efb2b9896d465464ba03996eceb1b0c0fb6fd5873926d9d1`  
		Last Modified: Wed, 21 Aug 2024 01:10:38 GMT  
		Size: 13.7 MB (13702007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32b10068afd288b7e7d37498071a10670e0113e78926909b2cb54ef23e4bc37`  
		Last Modified: Wed, 21 Aug 2024 01:10:37 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.2` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.2` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2-oracle`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.2-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2-oraclelinux9`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.2-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oracle`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.1` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1-oracle`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1-oraclelinux9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:a21ca6952f45280c948fec709d499acffec0dbc2a55817e1ef866bd6fc12c01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9e405223fe06f2a421ecbad9d467f9c1c258605a5ea5b1f3958b7b85aaf9a0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169460571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c0b42e12aecf9923bc295d49e2b8904d827bca6d7275714339995b6bdf8850c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66f57e79e60936d26459ed9997f8bd326eac42bd2cd859115c1ac5333ff2e11`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa602f88d6e0fa7d97bea12560009a08151b72543c39318e233214ccc940b513`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 6.7 MB (6711416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11985626def4e28561fcda9ac002e9855b85b135e734844faef443540beea7b`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882f6ee5042f9f988843ff67adccc33f3dccdd616a6774ac6a3216355a945541`  
		Last Modified: Wed, 21 Aug 2024 01:06:51 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc8a736f40d8920ad05b5a75eed7e49918f2c3cc996878f5f17924dd0fffb9f`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 47.2 MB (47234387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68528bb4bb6f6002d598d4b03fc38617ef1f240258f8d09c4844e41f5519439`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 319.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8648efaf486e3f158d1d5d86e18fbdcf5fb13857438f57450c110b84f6a831e`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 65.5 MB (65527474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67c74d61d10e2b23d8f3d49f7c73301f8b01fce59c1e6021fef0a9b8accc925`  
		Last Modified: Wed, 21 Aug 2024 01:06:52 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:44c7dce1f2fee299a81dad32f119fdb595efeb240cae35137daa5ea6fa4492e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32244a781790879f8ded9632059d176264700cffc35731b30983e3cc1b2b6f`

```dockerfile
```

-	Layers:
	-	`sha256:34497c01a017011c91fa7dec1348368fa8c2609652fdb4a7542b09dd4c5a0ccc`  
		Last Modified: Wed, 21 Aug 2024 01:06:53 GMT  
		Size: 13.8 MB (13816946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd61caa713fdf0f53c976c0df771b1a6e65406cc10af293672d437b776b0bf3c`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:9d7f3a4135babfc45623e4cc6a285d54631be4f82622468b211bd6657f84d906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166745650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f2d8a8c31f9698a209f82b78c3642ae6def6e65142cb3c05f101c923f6453b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:32:47 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c3e69b41776f9a4ede4dbc7c4ec3eca135765df8c489df178e4fbe5e1e3da`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e801bf8ccd081ec015487e133ba856b8c0f6d6c07247cdec5c59fc5453e03243`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 46.1 MB (46125256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aeb43cdaac42fa787548c0f92af67df0f466fafb46fc99251193a7c3aec78e0`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbc050cd8b2d786962b5666687f7af75158e5586ff47264918908c6110da511`  
		Last Modified: Wed, 21 Aug 2024 01:09:19 GMT  
		Size: 65.7 MB (65728998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362883ecd37835f2485fea9b8d3add3ff563539cfb8eeb63eec075a5250b30e`  
		Last Modified: Wed, 21 Aug 2024 01:09:18 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:caea2685500b09b9ca06ed522ec7f5c3e9484b129c2114382fdcfe1bd2b7b896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f68790acefae1362900254ff722a620fdbb8cc33b6948d0194b5670b647eda`

```dockerfile
```

-	Layers:
	-	`sha256:4876ead8f8ff75f4a65dffc89a10ded4da339bd11e4b4f94d040fa9a2e8442dd`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 13.8 MB (13812096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8eadaeb730cfe98f873a216aa60db0b677c22ba104364df2a8a5dbae07a15c`  
		Last Modified: Wed, 21 Aug 2024 01:09:17 GMT  
		Size: 34.5 KB (34475 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:9ceea965bd96a49b4299b8515fd92c3dc8ab26f34563795a350aae422985ea91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:9dc25923527a49b8de140a9e208faf7f00c0b21514b23e6569d53c63d1d50b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170262241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a6bffb6c998c5ffd6c88481981e0a037741d44907152ea2e94d5722613234c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:d32d33e9a4a3c5b65ff1ee9ecfd2216bcf6a92bfa1fa4e94e78d7fe79684e5c4 in / 
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
	-	`sha256:46047108b82f7aad92adc06b2f822db5457c57ebd6206e057de90f5a16e190f1`  
		Last Modified: Wed, 21 Aug 2024 00:30:26 GMT  
		Size: 49.0 MB (48994821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca4981e4b685b037b11a83e03ccfe5a76b07c9334ea30eed43d5c4cd350a417`  
		Last Modified: Wed, 21 Aug 2024 01:06:50 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb864cc9a3bd2dde9a981b5f4729a03a9b8370a8fb02c837d6fe16211174886`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b934a1f907becd6f478b6bc6b703dfb83629fe0a171fa9a696004cf47717f0e`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 6.7 MB (6711430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acadb43dd051779979829023f65806eaad0443bce2e9bf60e05f70cf18b54df`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 2.6 KB (2602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fe22960d72c3cc4519cfbc8a6997603938f683c28ec2dc7dda8bc4ae8bc463`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856e7a4274447dfe0a40b441f65c03a184244f3daecf22e103bbb1e93f9515f`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 47.7 MB (47690153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb79212beaf4ce96310fe9ec8b94df644a8d922d19745ac32f1d991e64843d9`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885acf912a94f1a04dd5426568bebfc394244d1a0c345f1ba82fb5ebb60a7626`  
		Last Modified: Wed, 21 Aug 2024 01:07:19 GMT  
		Size: 65.9 MB (65873358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbb350c706285b27404c845f80963694d9d4db32a2dc410c9ac16832ac1ebff`  
		Last Modified: Wed, 21 Aug 2024 01:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2dd20e303aa6a9a70c80cdce337e1ffb12c07d4b57cba48a59b30afe6ff71741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddddafdde7a83093655088189b9a6b815cee46b6f41a75c9b442088f77a42411`

```dockerfile
```

-	Layers:
	-	`sha256:449f7555a5f84e6d81dc011f386235b924403ee1f1e865c9af1e1d8ecd5f0aaa`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 13.8 MB (13820563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7f9481aa981cc50282578a3e844269f38ef02c302baa33e19427575ae5b71cb`  
		Last Modified: Wed, 21 Aug 2024 01:07:17 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:29a6f361e800231d32d4624395e9e98c2d346cbfe9f37864016b53bc33decab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167528878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affb2bfc837e9a7361c9df387b89eb37a0b769001f8cb1bd0fa9abb71fdd56ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:36:10 GMT
ADD file:149fb08a306c3560cfbfae2e22b15e97f0e1902b4888eddd201097a43351caa9 in / 
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
	-	`sha256:4b19fb6eb45f1444ac4b59114ce47de95db53a1bf5c59457ebc84557bbc2341e`  
		Last Modified: Tue, 20 Aug 2024 23:41:52 GMT  
		Size: 47.7 MB (47654566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcce6402af6a83eb533e9182f216fa5b9db7c3e057a4999c98bf11f812d638`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6133ef8f5f938ae359ff7df8610c2cb3a58aa7a2b2811228bfc2c50c2772d006`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4d202196ebd1d8200bbf6d2673a9dbbc2cdc38474433e28cccab9c659150d2`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 6.3 MB (6313917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c44f653f1c4313b40159761dabe6c1012c791d6a5bb7bcd38f42274b03fbacf`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b394d9fd8cd54292151d463f653c6f42ca47ea2f0cafede81b3cbbf703a5dd97`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c130709c94e50dc69e7c8d7d78923fa17c7cfafd7410ed52f5539e8de93e2ad5`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 46.6 MB (46581568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06ef2860059f2b1ed77483e2f97114a2fa3dc8f2d333bdd948c592ae3420bf5b`  
		Last Modified: Wed, 21 Aug 2024 01:07:57 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c4e968e873574a849dad79bdc20ac439e4e26903e1af8633c450465296dd4b`  
		Last Modified: Wed, 21 Aug 2024 01:07:59 GMT  
		Size: 66.1 MB (66055908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02ede93afa6fa1da188907383ac3f5c19a6797df4936fcbbbba2faf252aef0`  
		Last Modified: Wed, 21 Aug 2024 01:07:58 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:7074c3c778d62cef28870c6018d559c21a24905a8b6cb0d64a4f9878f5d28bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13851328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac3c71581b77db2e81ea1b222338aadc792276af410f008a372497486bc441a`

```dockerfile
```

-	Layers:
	-	`sha256:ca417120b66da7fd75b026dc826e4d9a45e4451a683215d63b7ded456c607b6f`  
		Last Modified: Wed, 21 Aug 2024 01:07:56 GMT  
		Size: 13.8 MB (13815749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76c89fdeab249fdc26db3da969e9fd14e616c0001790dab5b0d07ef47b6ef491`  
		Last Modified: Wed, 21 Aug 2024 01:07:55 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
