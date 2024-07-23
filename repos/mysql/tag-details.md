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
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:3e2592bb97cbd44edbcb5ca43029df0df90defd331122efd3a62bf9e38e2109c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:7b4902b99989615deaa12a3af4e32f21e9b32a862d6856d121dd44ca71c166ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b013c7c67d3b04af02965f22eea2f35279b4a5c39a2eec6698a840c511b042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ccc83ce1d0ea4779be24a3aff919964abaf81891e8c825ead145eee354c2c`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ae2ef29c4cc894852ece4424b79d983ae2ecd2e018fdb30e5422d03a6f2f7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aa9898aa1d99a6bbf41ae72a00b6ef17262cd1462525fd15f52820babdab2`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 6.7 MB (6711665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0229fb4f83ef39e5908a727c92adfafe7d04bd43a6bae09daf707e5e7d1bbdf`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfea4c359d4bed5bf53d8bf0db4e9c3ab2d5aad20410ef68568a379efe8b4b1`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe59aa1e5c672c007ed012f05395aadff0ff9a7cb1c07af82b1c96eb08179a`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 49.2 MB (49164037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336dce1c47f1785cde00a55945a44d964229eaca71359368fcdc1e7fd434fd5`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71c9d185d1c6671545affa5a0b02c6a67d10ed0d8d899303940d3ea5264781`  
		Last Modified: Tue, 23 Jul 2024 00:08:04 GMT  
		Size: 60.9 MB (60920136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d4802c63b9f8b11ea0933046b1e2d0e4d34af269c6de02e006674038a8aab`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f329967ab0c553cc2cfc4fbbb879d2f569641985b0e70fd2b6bb638c6cd79`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:30f69f041679b720f2b263ddb7c40daf6bd1f90503a5589c8f23efd138f05064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563997cb919d22a95052f78fd4bd1401e58c36ad8da1b28eda9444f7f4d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f6704744ddeb11d0ffa247f25a5d266a2284c67b9d26b90a33064b3f8f426180`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 13.7 MB (13706897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762eeea3ad5905a68baf6fe4fe7bb0c71cc7f81ba8c0a1f15f747809a9fbc6e9`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b79e215f62998bf3b796d4f1db3bf92a1494f04e458df56a5f88dafc7a3f8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171317802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefa4e35197d018d0130f88916c7454967edd8ea149eedd108bfc9c4382f6026`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:16:15 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29e21a87dbdeb125b08b366dbb08a93c8140370b7f482e8007fcff8f4d2e43f`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c58fcb53d94d8cf681f340273935a53560a4224686b0e92d6e7ef519bbabca`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 48.0 MB (48031386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ed9981deb067ded188f629847e6a11623fcb57bca8fc274f3f122245fd09de`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f4cb1ffd70c3d44fa3800777042683abfb30ce82a4bb4908a85e048a5709c`  
		Last Modified: Tue, 09 Jul 2024 00:00:35 GMT  
		Size: 68.4 MB (68396174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d9ddb9406fc79769da373e84ee1b56f63adbf9d8699695ac070f6b71f1a4c`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda302a1deb9bf91752f792622ef6f5dc9c91c170e4511afe6182a220b994a7`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:4533f7e6364de330848bd456d22d6e9950c1d6bd26a615807f2ec78d07177bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8dfc34416f440f6b52634a4c47157abda32780394260ac156c88ec42655716`

```dockerfile
```

-	Layers:
	-	`sha256:181817efb7e37537010b183a966f783c2b9b7be871b70a605c2891df931efc19`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2389e16e1321c02f07cd8753005a428746e2ba7c853a98b0761598c5a7685c1e`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:04805c6af59d7b087d464da1ccf359fd1e0a6d60513df2362219b1289fa8d172
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:74d24f79fafbb3682a6f64683b2303d9c3abbf5bdd477b2b237c44dca78890f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184731709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a5ac32be1d10e2bc922fc1b863b4d488960db1490ed8886e283cc68e3f386e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca1fa2dd574c407d190a86bfa21b56fbd83c35cee891f7cf57fb0d330a505a`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15531fdc99b65aac65dc0c61b21b37c598091e1b732eb3d2ba9007452fce6d`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.4 MB (4422749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e463a7aebaa1c76df4a284a7d58d61ec4b5d78adf6308196e8bd459ab04fa935`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.4 MB (1445924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f620cd6ca53aed53be58751620f3d41d125cbebf6486df8c00d147aa5ff0dbbe`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144d0ea1132f37fb860f00a0cf38cd63ca5fd5e9a4fc37c70c2bcb9ac26973c`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 15.3 MB (15285091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76437961ba842da55ca42721fdd16385f92473387fa2914c8ed4f571c1aca73`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ee3a7c0bd86b2bbbba03b55b1b1824644a58e1c9161cbdf08bcec7959d1c5`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864718177bd6a3e599167787a04e5a032d392e91fb7ae9d4bf2c1b517f4ecc24`  
		Last Modified: Tue, 23 Jul 2024 07:15:22 GMT  
		Size: 134.4 MB (134441392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebee5787f4417c60ac8f10345ab7143a79cc2a7879731e51a4b9cac4c0fbb79`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca6353f1aedec4e26002c6c8d50ac528e03b9cbfa7fd23f950019d7bcf51db3`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c00ad7e2e80533227b1ba473ed0603fa9559317fef5fdda4ef96d55949609c`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:6edbcdb7bf0bfe7e018c36f0ab054190b17cb70240e3a46d476aa2765cd6b1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98205d4c3f39171e620a53cf01e407d2d23483787ce997ffe5fc03c4939273c3`

```dockerfile
```

-	Layers:
	-	`sha256:b12fbbfd9808135ae28b137aa84d1eb2906dbaed2a8e37caf962eef3eea2120e`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dada0af205573493cf9033d29b747c66ed6374e24ef910be844d3db821d00b6b`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:04805c6af59d7b087d464da1ccf359fd1e0a6d60513df2362219b1289fa8d172
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:74d24f79fafbb3682a6f64683b2303d9c3abbf5bdd477b2b237c44dca78890f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184731709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a5ac32be1d10e2bc922fc1b863b4d488960db1490ed8886e283cc68e3f386e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca1fa2dd574c407d190a86bfa21b56fbd83c35cee891f7cf57fb0d330a505a`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15531fdc99b65aac65dc0c61b21b37c598091e1b732eb3d2ba9007452fce6d`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.4 MB (4422749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e463a7aebaa1c76df4a284a7d58d61ec4b5d78adf6308196e8bd459ab04fa935`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.4 MB (1445924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f620cd6ca53aed53be58751620f3d41d125cbebf6486df8c00d147aa5ff0dbbe`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144d0ea1132f37fb860f00a0cf38cd63ca5fd5e9a4fc37c70c2bcb9ac26973c`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 15.3 MB (15285091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76437961ba842da55ca42721fdd16385f92473387fa2914c8ed4f571c1aca73`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ee3a7c0bd86b2bbbba03b55b1b1824644a58e1c9161cbdf08bcec7959d1c5`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864718177bd6a3e599167787a04e5a032d392e91fb7ae9d4bf2c1b517f4ecc24`  
		Last Modified: Tue, 23 Jul 2024 07:15:22 GMT  
		Size: 134.4 MB (134441392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebee5787f4417c60ac8f10345ab7143a79cc2a7879731e51a4b9cac4c0fbb79`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca6353f1aedec4e26002c6c8d50ac528e03b9cbfa7fd23f950019d7bcf51db3`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c00ad7e2e80533227b1ba473ed0603fa9559317fef5fdda4ef96d55949609c`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:6edbcdb7bf0bfe7e018c36f0ab054190b17cb70240e3a46d476aa2765cd6b1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98205d4c3f39171e620a53cf01e407d2d23483787ce997ffe5fc03c4939273c3`

```dockerfile
```

-	Layers:
	-	`sha256:b12fbbfd9808135ae28b137aa84d1eb2906dbaed2a8e37caf962eef3eea2120e`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dada0af205573493cf9033d29b747c66ed6374e24ef910be844d3db821d00b6b`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:3e2592bb97cbd44edbcb5ca43029df0df90defd331122efd3a62bf9e38e2109c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7b4902b99989615deaa12a3af4e32f21e9b32a862d6856d121dd44ca71c166ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b013c7c67d3b04af02965f22eea2f35279b4a5c39a2eec6698a840c511b042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ccc83ce1d0ea4779be24a3aff919964abaf81891e8c825ead145eee354c2c`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ae2ef29c4cc894852ece4424b79d983ae2ecd2e018fdb30e5422d03a6f2f7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aa9898aa1d99a6bbf41ae72a00b6ef17262cd1462525fd15f52820babdab2`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 6.7 MB (6711665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0229fb4f83ef39e5908a727c92adfafe7d04bd43a6bae09daf707e5e7d1bbdf`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfea4c359d4bed5bf53d8bf0db4e9c3ab2d5aad20410ef68568a379efe8b4b1`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe59aa1e5c672c007ed012f05395aadff0ff9a7cb1c07af82b1c96eb08179a`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 49.2 MB (49164037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336dce1c47f1785cde00a55945a44d964229eaca71359368fcdc1e7fd434fd5`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71c9d185d1c6671545affa5a0b02c6a67d10ed0d8d899303940d3ea5264781`  
		Last Modified: Tue, 23 Jul 2024 00:08:04 GMT  
		Size: 60.9 MB (60920136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d4802c63b9f8b11ea0933046b1e2d0e4d34af269c6de02e006674038a8aab`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f329967ab0c553cc2cfc4fbbb879d2f569641985b0e70fd2b6bb638c6cd79`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:30f69f041679b720f2b263ddb7c40daf6bd1f90503a5589c8f23efd138f05064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563997cb919d22a95052f78fd4bd1401e58c36ad8da1b28eda9444f7f4d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f6704744ddeb11d0ffa247f25a5d266a2284c67b9d26b90a33064b3f8f426180`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 13.7 MB (13706897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762eeea3ad5905a68baf6fe4fe7bb0c71cc7f81ba8c0a1f15f747809a9fbc6e9`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b79e215f62998bf3b796d4f1db3bf92a1494f04e458df56a5f88dafc7a3f8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171317802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefa4e35197d018d0130f88916c7454967edd8ea149eedd108bfc9c4382f6026`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:16:15 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29e21a87dbdeb125b08b366dbb08a93c8140370b7f482e8007fcff8f4d2e43f`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c58fcb53d94d8cf681f340273935a53560a4224686b0e92d6e7ef519bbabca`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 48.0 MB (48031386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ed9981deb067ded188f629847e6a11623fcb57bca8fc274f3f122245fd09de`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f4cb1ffd70c3d44fa3800777042683abfb30ce82a4bb4908a85e048a5709c`  
		Last Modified: Tue, 09 Jul 2024 00:00:35 GMT  
		Size: 68.4 MB (68396174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d9ddb9406fc79769da373e84ee1b56f63adbf9d8699695ac070f6b71f1a4c`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda302a1deb9bf91752f792622ef6f5dc9c91c170e4511afe6182a220b994a7`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:4533f7e6364de330848bd456d22d6e9950c1d6bd26a615807f2ec78d07177bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8dfc34416f440f6b52634a4c47157abda32780394260ac156c88ec42655716`

```dockerfile
```

-	Layers:
	-	`sha256:181817efb7e37537010b183a966f783c2b9b7be871b70a605c2891df931efc19`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2389e16e1321c02f07cd8753005a428746e2ba7c853a98b0761598c5a7685c1e`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:3e2592bb97cbd44edbcb5ca43029df0df90defd331122efd3a62bf9e38e2109c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:7b4902b99989615deaa12a3af4e32f21e9b32a862d6856d121dd44ca71c166ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b013c7c67d3b04af02965f22eea2f35279b4a5c39a2eec6698a840c511b042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ccc83ce1d0ea4779be24a3aff919964abaf81891e8c825ead145eee354c2c`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ae2ef29c4cc894852ece4424b79d983ae2ecd2e018fdb30e5422d03a6f2f7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aa9898aa1d99a6bbf41ae72a00b6ef17262cd1462525fd15f52820babdab2`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 6.7 MB (6711665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0229fb4f83ef39e5908a727c92adfafe7d04bd43a6bae09daf707e5e7d1bbdf`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfea4c359d4bed5bf53d8bf0db4e9c3ab2d5aad20410ef68568a379efe8b4b1`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe59aa1e5c672c007ed012f05395aadff0ff9a7cb1c07af82b1c96eb08179a`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 49.2 MB (49164037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336dce1c47f1785cde00a55945a44d964229eaca71359368fcdc1e7fd434fd5`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71c9d185d1c6671545affa5a0b02c6a67d10ed0d8d899303940d3ea5264781`  
		Last Modified: Tue, 23 Jul 2024 00:08:04 GMT  
		Size: 60.9 MB (60920136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d4802c63b9f8b11ea0933046b1e2d0e4d34af269c6de02e006674038a8aab`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f329967ab0c553cc2cfc4fbbb879d2f569641985b0e70fd2b6bb638c6cd79`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:30f69f041679b720f2b263ddb7c40daf6bd1f90503a5589c8f23efd138f05064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563997cb919d22a95052f78fd4bd1401e58c36ad8da1b28eda9444f7f4d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f6704744ddeb11d0ffa247f25a5d266a2284c67b9d26b90a33064b3f8f426180`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 13.7 MB (13706897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762eeea3ad5905a68baf6fe4fe7bb0c71cc7f81ba8c0a1f15f747809a9fbc6e9`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:b79e215f62998bf3b796d4f1db3bf92a1494f04e458df56a5f88dafc7a3f8869
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171317802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefa4e35197d018d0130f88916c7454967edd8ea149eedd108bfc9c4382f6026`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:16:15 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.38-1.el9
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:16:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:16:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29e21a87dbdeb125b08b366dbb08a93c8140370b7f482e8007fcff8f4d2e43f`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c58fcb53d94d8cf681f340273935a53560a4224686b0e92d6e7ef519bbabca`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 48.0 MB (48031386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ed9981deb067ded188f629847e6a11623fcb57bca8fc274f3f122245fd09de`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665f4cb1ffd70c3d44fa3800777042683abfb30ce82a4bb4908a85e048a5709c`  
		Last Modified: Tue, 09 Jul 2024 00:00:35 GMT  
		Size: 68.4 MB (68396174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:912d9ddb9406fc79769da373e84ee1b56f63adbf9d8699695ac070f6b71f1a4c`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfda302a1deb9bf91752f792622ef6f5dc9c91c170e4511afe6182a220b994a7`  
		Last Modified: Tue, 09 Jul 2024 00:00:33 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:4533f7e6364de330848bd456d22d6e9950c1d6bd26a615807f2ec78d07177bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13712692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8dfc34416f440f6b52634a4c47157abda32780394260ac156c88ec42655716`

```dockerfile
```

-	Layers:
	-	`sha256:181817efb7e37537010b183a966f783c2b9b7be871b70a605c2891df931efc19`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 13.7 MB (13677580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2389e16e1321c02f07cd8753005a428746e2ba7c853a98b0761598c5a7685c1e`  
		Last Modified: Tue, 09 Jul 2024 00:00:32 GMT  
		Size: 35.1 KB (35112 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39`

```console
$ docker pull mysql@sha256:b69d51fd476c0a7f35ed213766aac24ddb5f9a07e8a32ca76b383d2f3dae8e76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39` - linux; amd64

```console
$ docker pull mysql@sha256:7b4902b99989615deaa12a3af4e32f21e9b32a862d6856d121dd44ca71c166ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b013c7c67d3b04af02965f22eea2f35279b4a5c39a2eec6698a840c511b042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ccc83ce1d0ea4779be24a3aff919964abaf81891e8c825ead145eee354c2c`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ae2ef29c4cc894852ece4424b79d983ae2ecd2e018fdb30e5422d03a6f2f7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aa9898aa1d99a6bbf41ae72a00b6ef17262cd1462525fd15f52820babdab2`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 6.7 MB (6711665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0229fb4f83ef39e5908a727c92adfafe7d04bd43a6bae09daf707e5e7d1bbdf`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfea4c359d4bed5bf53d8bf0db4e9c3ab2d5aad20410ef68568a379efe8b4b1`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe59aa1e5c672c007ed012f05395aadff0ff9a7cb1c07af82b1c96eb08179a`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 49.2 MB (49164037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336dce1c47f1785cde00a55945a44d964229eaca71359368fcdc1e7fd434fd5`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71c9d185d1c6671545affa5a0b02c6a67d10ed0d8d899303940d3ea5264781`  
		Last Modified: Tue, 23 Jul 2024 00:08:04 GMT  
		Size: 60.9 MB (60920136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d4802c63b9f8b11ea0933046b1e2d0e4d34af269c6de02e006674038a8aab`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f329967ab0c553cc2cfc4fbbb879d2f569641985b0e70fd2b6bb638c6cd79`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39` - unknown; unknown

```console
$ docker pull mysql@sha256:30f69f041679b720f2b263ddb7c40daf6bd1f90503a5589c8f23efd138f05064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563997cb919d22a95052f78fd4bd1401e58c36ad8da1b28eda9444f7f4d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f6704744ddeb11d0ffa247f25a5d266a2284c67b9d26b90a33064b3f8f426180`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 13.7 MB (13706897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762eeea3ad5905a68baf6fe4fe7bb0c71cc7f81ba8c0a1f15f747809a9fbc6e9`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-bookworm`

```console
$ docker pull mysql@sha256:04805c6af59d7b087d464da1ccf359fd1e0a6d60513df2362219b1289fa8d172
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:74d24f79fafbb3682a6f64683b2303d9c3abbf5bdd477b2b237c44dca78890f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184731709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a5ac32be1d10e2bc922fc1b863b4d488960db1490ed8886e283cc68e3f386e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca1fa2dd574c407d190a86bfa21b56fbd83c35cee891f7cf57fb0d330a505a`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15531fdc99b65aac65dc0c61b21b37c598091e1b732eb3d2ba9007452fce6d`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.4 MB (4422749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e463a7aebaa1c76df4a284a7d58d61ec4b5d78adf6308196e8bd459ab04fa935`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.4 MB (1445924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f620cd6ca53aed53be58751620f3d41d125cbebf6486df8c00d147aa5ff0dbbe`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144d0ea1132f37fb860f00a0cf38cd63ca5fd5e9a4fc37c70c2bcb9ac26973c`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 15.3 MB (15285091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76437961ba842da55ca42721fdd16385f92473387fa2914c8ed4f571c1aca73`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ee3a7c0bd86b2bbbba03b55b1b1824644a58e1c9161cbdf08bcec7959d1c5`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864718177bd6a3e599167787a04e5a032d392e91fb7ae9d4bf2c1b517f4ecc24`  
		Last Modified: Tue, 23 Jul 2024 07:15:22 GMT  
		Size: 134.4 MB (134441392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebee5787f4417c60ac8f10345ab7143a79cc2a7879731e51a4b9cac4c0fbb79`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca6353f1aedec4e26002c6c8d50ac528e03b9cbfa7fd23f950019d7bcf51db3`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c00ad7e2e80533227b1ba473ed0603fa9559317fef5fdda4ef96d55949609c`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:6edbcdb7bf0bfe7e018c36f0ab054190b17cb70240e3a46d476aa2765cd6b1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98205d4c3f39171e620a53cf01e407d2d23483787ce997ffe5fc03c4939273c3`

```dockerfile
```

-	Layers:
	-	`sha256:b12fbbfd9808135ae28b137aa84d1eb2906dbaed2a8e37caf962eef3eea2120e`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dada0af205573493cf9033d29b747c66ed6374e24ef910be844d3db821d00b6b`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-debian`

```console
$ docker pull mysql@sha256:04805c6af59d7b087d464da1ccf359fd1e0a6d60513df2362219b1289fa8d172
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39-debian` - linux; amd64

```console
$ docker pull mysql@sha256:74d24f79fafbb3682a6f64683b2303d9c3abbf5bdd477b2b237c44dca78890f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184731709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a5ac32be1d10e2bc922fc1b863b4d488960db1490ed8886e283cc68e3f386e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:32 GMT
ADD file:6c4730e7b12278bc7eb83b3b9d659437c92c42fc7ee70922ae8c4bebfb56a602 in / 
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
	-	`sha256:efc2b5ad9eec05befa54239d53feeae3569ccbef689aa5e5dbfc25da6c4df559`  
		Last Modified: Tue, 23 Jul 2024 05:27:55 GMT  
		Size: 29.1 MB (29126287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ca1fa2dd574c407d190a86bfa21b56fbd83c35cee891f7cf57fb0d330a505a`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c15531fdc99b65aac65dc0c61b21b37c598091e1b732eb3d2ba9007452fce6d`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.4 MB (4422749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e463a7aebaa1c76df4a284a7d58d61ec4b5d78adf6308196e8bd459ab04fa935`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 1.4 MB (1445924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f620cd6ca53aed53be58751620f3d41d125cbebf6486df8c00d147aa5ff0dbbe`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f144d0ea1132f37fb860f00a0cf38cd63ca5fd5e9a4fc37c70c2bcb9ac26973c`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 15.3 MB (15285091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76437961ba842da55ca42721fdd16385f92473387fa2914c8ed4f571c1aca73`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9ee3a7c0bd86b2bbbba03b55b1b1824644a58e1c9161cbdf08bcec7959d1c5`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864718177bd6a3e599167787a04e5a032d392e91fb7ae9d4bf2c1b517f4ecc24`  
		Last Modified: Tue, 23 Jul 2024 07:15:22 GMT  
		Size: 134.4 MB (134441392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebee5787f4417c60ac8f10345ab7143a79cc2a7879731e51a4b9cac4c0fbb79`  
		Last Modified: Tue, 23 Jul 2024 07:15:19 GMT  
		Size: 843.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca6353f1aedec4e26002c6c8d50ac528e03b9cbfa7fd23f950019d7bcf51db3`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 5.3 KB (5323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c00ad7e2e80533227b1ba473ed0603fa9559317fef5fdda4ef96d55949609c`  
		Last Modified: Tue, 23 Jul 2024 07:15:20 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:6edbcdb7bf0bfe7e018c36f0ab054190b17cb70240e3a46d476aa2765cd6b1b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98205d4c3f39171e620a53cf01e407d2d23483787ce997ffe5fc03c4939273c3`

```dockerfile
```

-	Layers:
	-	`sha256:b12fbbfd9808135ae28b137aa84d1eb2906dbaed2a8e37caf962eef3eea2120e`  
		Last Modified: Tue, 23 Jul 2024 07:15:18 GMT  
		Size: 4.0 MB (3981559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dada0af205573493cf9033d29b747c66ed6374e24ef910be844d3db821d00b6b`  
		Last Modified: Tue, 23 Jul 2024 07:15:17 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-oracle`

```console
$ docker pull mysql@sha256:b69d51fd476c0a7f35ed213766aac24ddb5f9a07e8a32ca76b383d2f3dae8e76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:7b4902b99989615deaa12a3af4e32f21e9b32a862d6856d121dd44ca71c166ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b013c7c67d3b04af02965f22eea2f35279b4a5c39a2eec6698a840c511b042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ccc83ce1d0ea4779be24a3aff919964abaf81891e8c825ead145eee354c2c`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ae2ef29c4cc894852ece4424b79d983ae2ecd2e018fdb30e5422d03a6f2f7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aa9898aa1d99a6bbf41ae72a00b6ef17262cd1462525fd15f52820babdab2`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 6.7 MB (6711665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0229fb4f83ef39e5908a727c92adfafe7d04bd43a6bae09daf707e5e7d1bbdf`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfea4c359d4bed5bf53d8bf0db4e9c3ab2d5aad20410ef68568a379efe8b4b1`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe59aa1e5c672c007ed012f05395aadff0ff9a7cb1c07af82b1c96eb08179a`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 49.2 MB (49164037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336dce1c47f1785cde00a55945a44d964229eaca71359368fcdc1e7fd434fd5`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71c9d185d1c6671545affa5a0b02c6a67d10ed0d8d899303940d3ea5264781`  
		Last Modified: Tue, 23 Jul 2024 00:08:04 GMT  
		Size: 60.9 MB (60920136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d4802c63b9f8b11ea0933046b1e2d0e4d34af269c6de02e006674038a8aab`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f329967ab0c553cc2cfc4fbbb879d2f569641985b0e70fd2b6bb638c6cd79`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:30f69f041679b720f2b263ddb7c40daf6bd1f90503a5589c8f23efd138f05064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563997cb919d22a95052f78fd4bd1401e58c36ad8da1b28eda9444f7f4d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f6704744ddeb11d0ffa247f25a5d266a2284c67b9d26b90a33064b3f8f426180`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 13.7 MB (13706897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762eeea3ad5905a68baf6fe4fe7bb0c71cc7f81ba8c0a1f15f747809a9fbc6e9`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.39-oraclelinux9`

```console
$ docker pull mysql@sha256:b69d51fd476c0a7f35ed213766aac24ddb5f9a07e8a32ca76b383d2f3dae8e76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.39-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:7b4902b99989615deaa12a3af4e32f21e9b32a862d6856d121dd44ca71c166ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166782167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b013c7c67d3b04af02965f22eea2f35279b4a5c39a2eec6698a840c511b042`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ccc83ce1d0ea4779be24a3aff919964abaf81891e8c825ead145eee354c2c`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98ae2ef29c4cc894852ece4424b79d983ae2ecd2e018fdb30e5422d03a6f2f7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1aa9898aa1d99a6bbf41ae72a00b6ef17262cd1462525fd15f52820babdab2`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 6.7 MB (6711665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0229fb4f83ef39e5908a727c92adfafe7d04bd43a6bae09daf707e5e7d1bbdf`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfea4c359d4bed5bf53d8bf0db4e9c3ab2d5aad20410ef68568a379efe8b4b1`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6fe59aa1e5c672c007ed012f05395aadff0ff9a7cb1c07af82b1c96eb08179a`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 49.2 MB (49164037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7336dce1c47f1785cde00a55945a44d964229eaca71359368fcdc1e7fd434fd5`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c71c9d185d1c6671545affa5a0b02c6a67d10ed0d8d899303940d3ea5264781`  
		Last Modified: Tue, 23 Jul 2024 00:08:04 GMT  
		Size: 60.9 MB (60920136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63d4802c63b9f8b11ea0933046b1e2d0e4d34af269c6de02e006674038a8aab`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f329967ab0c553cc2cfc4fbbb879d2f569641985b0e70fd2b6bb638c6cd79`  
		Last Modified: Tue, 23 Jul 2024 00:08:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.39-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:30f69f041679b720f2b263ddb7c40daf6bd1f90503a5589c8f23efd138f05064
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13741678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563997cb919d22a95052f78fd4bd1401e58c36ad8da1b28eda9444f7f4d6870`

```dockerfile
```

-	Layers:
	-	`sha256:f6704744ddeb11d0ffa247f25a5d266a2284c67b9d26b90a33064b3f8f426180`  
		Last Modified: Tue, 23 Jul 2024 00:08:02 GMT  
		Size: 13.7 MB (13706897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:762eeea3ad5905a68baf6fe4fe7bb0c71cc7f81ba8c0a1f15f747809a9fbc6e9`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2`

```console
$ docker pull mysql@sha256:96709bc0805dde3353089d2439f9dc617440bd2309a6f595bb5af40d65d4918e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.4.2` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2-oracle`

```console
$ docker pull mysql@sha256:96709bc0805dde3353089d2439f9dc617440bd2309a6f595bb5af40d65d4918e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.4.2-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.2-oraclelinux9`

```console
$ docker pull mysql@sha256:96709bc0805dde3353089d2439f9dc617440bd2309a6f595bb5af40d65d4918e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.4.2-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.2-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oracle`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oraclelinux9`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1`

```console
$ docker pull mysql@sha256:c62d73c5b79a11257fac4eae5af12cb36628a0f197a96e44481dd78f27404a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0.1` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1-oracle`

```console
$ docker pull mysql@sha256:c62d73c5b79a11257fac4eae5af12cb36628a0f197a96e44481dd78f27404a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.1-oraclelinux9`

```console
$ docker pull mysql@sha256:c62d73c5b79a11257fac4eae5af12cb36628a0f197a96e44481dd78f27404a37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:29c19d850ef49f69aaf0e586a06ac3fbadd2e16486aaaeb26bf27697be925b47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a25663df56ae13e472b4af2395daf14d355831854dcaee82b222719efe2f5927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169463072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:233a484acc79daf2d74ea6eb4f702bbbaea5f092c0b102a70dfe23bd4a172d8b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53642a0022d5c063bebb52d0076183ef6bb00dac0699c5600b33b61fd97d128`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e014db4952e5a125ab953a771a8afefeb359e4834386ed915532e833572349d0`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eafd2923747a1d36938e140350aecf88a4242b804556170b0a6825c00f2df4c3`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 6.7 MB (6711720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c04ec8be374eed66387dcb49426e74239e7fad714e80f6175a44fd949341c4`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9a13924bdf5d6a3cd4470e2717dbcf13553ba52268f42d4c98172ae8acbf38`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02447e7bb1e300f3d64740cd805a46dde904f38756f4bb64f1ceb3ffaf01c46b`  
		Last Modified: Tue, 23 Jul 2024 00:07:59 GMT  
		Size: 47.2 MB (47236698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9089cc93f620559b2e74235a9eb7554c55b8f8dc5f7996abb6226f8e21ef4dfd`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b156cf22ba85eda85e20c7656543432041c93f208355d9606c4ad21121c6b7`  
		Last Modified: Tue, 23 Jul 2024 00:08:01 GMT  
		Size: 65.5 MB (65528440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613f509a6df738b9782732175190eb7df29944099651998c434ab48b54fd622f`  
		Last Modified: Tue, 23 Jul 2024 00:07:58 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1941dec23e9d0e7660afa5920cfea4c2aafefae63b08adffce475af49990f757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5b64067623b99a1a5f0a26687d16c0ce351ad07850ddfaf44be63adee2a8ab8`

```dockerfile
```

-	Layers:
	-	`sha256:064936866f98b7a3d17acb5c3484b698433e93aa75c2ea00206f1d7b7b3f3d97`  
		Last Modified: Tue, 23 Jul 2024 00:07:57 GMT  
		Size: 13.8 MB (13816914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:731eb3ff2666f5886f7a8fe02812fee35f8938b080d918b655447c3cae2a3a9f`  
		Last Modified: Tue, 23 Jul 2024 00:07:56 GMT  
		Size: 34.1 KB (34072 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:2e8268487ee2bcf7f2fb696578143a75371a021668aa0b04780e72d72f3187ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.7 MB (166736379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d237f79428a6a777564658780cf246a341f6db3fe1798f9be81240593f9dbdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 04:20:59 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENV MYSQL_SHELL_VERSION=8.4.1-1.el9
# Tue, 02 Jul 2024 04:20:59 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:20:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 04:20:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 04:20:59 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 04:20:59 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aac7d685a2a63fb388450cb427aa34bd1d12c111e2571226850ca2271ab8697`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e3581bc157b4f5452fa33fe3ffe2f93744005f2993fbd9ae5e62b739c1e15`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 46.1 MB (46116070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575080e22a6fce69b25417c0c5c52ac673ea62d1e0083d7f43cebe01f1ea938e`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d1cfd2059083a906906e424b189913b4b78b60f6463dace8a8b3fb583bc75f`  
		Last Modified: Mon, 08 Jul 2024 23:59:16 GMT  
		Size: 65.7 MB (65730185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8402c954594ce3e57cb9c1f448c019f80e6c6e42f2b005f332778cb2f02ddfc2`  
		Last Modified: Mon, 08 Jul 2024 23:59:15 GMT  
		Size: 5.3 KB (5326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:72d8606e966a37da8f7ff1c1ffd3e00765dffcb6ff1bafd85c50f55ed61c3336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13822145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5706f5b034ff86383a97adf78eddd48260f1f9e6b0482534052a6879a533779d`

```dockerfile
```

-	Layers:
	-	`sha256:f58a9e0828789b0e90aeb59533e3dce0c49049df151475c960428b2706c6f947`  
		Last Modified: Mon, 08 Jul 2024 23:59:14 GMT  
		Size: 13.8 MB (13787669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64e292419a6f47602a63cc4fb74b859e620172fc7f9ba9117680043ae8e0203a`  
		Last Modified: Mon, 08 Jul 2024 23:59:13 GMT  
		Size: 34.5 KB (34476 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:76cfe72d2c51be8946bbd3085028e8989599bae0c6112748c1da35ad448fc00b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:40e3265a989949477b1c5c7386b99e957545636c5313dac7a849a0fcbb05d9a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170258720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ce93a845a8a98c89bd58a5e45fe71277ca5f52177c88046858a6a0af969ba74`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
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
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b01031aab669fe390dbf3937367ac492b921b6781c8e0c4c8b0d16c427490`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa72c34c4347e05d6ff71ec082b8db4999ad05e93543032dbf132f5b45406cb1`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ade985fa2a84e8415767d0cb85c9ac769457c8a591b26f41e656918aaa9d6`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 6.7 MB (6711705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc168a9482de470f142da0db506b4a6877c4cc17b1f4173e906893d8db5d5fa3`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 2.6 KB (2609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca3786815ddffdc8271f5e723e3822d29d21d6c7d2d408ff5c302baedd5ebef`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 338.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fac98ea8376cab3fa8e647bace80a616bff77d4c6c909bbbf2b2e247b870f`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 47.7 MB (47695390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e5505c3ae424fc101215f5c28d6df334b5344d8715d9d6af9a34d8264627a1`  
		Last Modified: Tue, 23 Jul 2024 00:07:53 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79ade39aab9324ad36c9c59f76ce2ae705fcdfada3dad29f3dff0da9058b280`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 65.9 MB (65865405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae34d51c6da25fc42d28b272901ad6eb353a90223334b049c4065698e21dec1a`  
		Last Modified: Tue, 23 Jul 2024 00:07:54 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:42659624650b54d9878e5ea7b705058a2cacb93b89ec9cfb5b00e8bdb1050b27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13855671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb81650ff4371b76815c0d0b4cef732f46457ab49ebb703210def1b9b534a357`

```dockerfile
```

-	Layers:
	-	`sha256:90238cd398e6744d53600a23803ef64baa27a5134067321a44523269e9261fcc`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 13.8 MB (13820531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a32f744c8ddf78ea595a31af7eaf88700221e4dc2a922bafafc5eaf61d625471`  
		Last Modified: Tue, 23 Jul 2024 00:07:52 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:aada4820513123bcae9e64a29bba209f562c62660e59e36f2b7846b8d8417885
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.5 MB (167542082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3239d2b6d8873ddf5c422796fdc4f8b6475695e2b3ebb0011a2fad909a81921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 09:20:08 GMT
ADD file:a5d614a69430ac76660689e833533429bd70568280b25af98af60b01a76d6139 in / 
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["/bin/bash"]
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_MAJOR=innovation
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysqlinnovation-server-minimal]'; 		echo 'name=MySQL innovation Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-innovation-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-innovation-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENV MYSQL_SHELL_VERSION=9.0.0-1.el9
# Tue, 02 Jul 2024 09:20:08 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 09:20:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 09:20:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 09:20:08 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 02 Jul 2024 09:20:08 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:c72f53f7235bf26fdb27eaeb0d712fc1886f19eda2722ef9709dda7424814b9e`  
		Last Modified: Mon, 08 Jul 2024 22:41:23 GMT  
		Size: 47.7 MB (47652661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e4ed755af29fc091f6b3f3a295d7eb6d9f70ce20e10f15ea560a61c89f5511`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 879.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8c802f90bcb55a56c8fc6eba20da29fec657eb2bff8a6e5352dbb7e4ad6062`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 913.4 KB (913441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eecc55f854cdab91d64d65c97cbb146c14612d9a5de8d677864c78060bf8cb37`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 6.3 MB (6314558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8dabc098139106214f4e20e771ae59487a508120e3c1296492b94d869f296b`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a27c3f0dbd7bd618d96252fb302dc315239f2bd5342fb24503fcb8355e1bb00`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55978eb4258b58e8175bccf79076058dcc239db7dbf4b6a7097ea079d109972`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 46.6 MB (46592514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767d62f87325416c2ebc22b63cd89796fde8c27f24e64fac684f11afb5cbbdca`  
		Last Modified: Mon, 08 Jul 2024 23:57:54 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe5d39ea75cdaa6f800950068c7131523356cf366be712a99f1b6b672a29589`  
		Last Modified: Mon, 08 Jul 2024 23:57:56 GMT  
		Size: 66.1 MB (66059432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72a1a98f7aad5e2bdaf2d8d1d4adfaae73a57d7480814dc93a89810cc594bbf9`  
		Last Modified: Mon, 08 Jul 2024 23:57:55 GMT  
		Size: 5.3 KB (5327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:ac6409a8328fc8f115b4fbf0764e981aaabb371fb76a0885e79b437eed76497f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7a2c605428149e58f3c2e4afb2004e1b05b27d02b249b33825eed3ab343036a`

```dockerfile
```

-	Layers:
	-	`sha256:c5f9e58d98d85132ddf253ac2d075b8662dc4172f2a5111b8ae9ef7d43ec7f13`  
		Last Modified: Mon, 08 Jul 2024 23:57:53 GMT  
		Size: 13.8 MB (13791322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:968648cfa994bb2b9c97f0b1d5b7aaf9f5b76ff23e4e441180974ac90a166a91`  
		Last Modified: Mon, 08 Jul 2024 23:57:52 GMT  
		Size: 35.6 KB (35579 bytes)  
		MIME: application/vnd.in-toto+json
