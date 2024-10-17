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
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:bf79508626d6cad5bd82ea762109690e42467b1eefedab27946eccd69ab23069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:1c9a74f109e3f0652a74e26835d483cf43412611a0c9895e03ee6694a6703698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170572138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d6b00bceda8e96d5a84590808ba2cb6dca6c020971ed438e50ac3af798c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6111251d1d05a298b2e671590545d81d77f605a0909a7a78131c0639d1aa6dd7`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669648c0f2f15956edcf8b8789c3603322ef63cb3bb77d558add2b4848858bf`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19c425e6ff82725f7cce8c81138dad656b6efff512313e3b80402fb9da218d`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 6.7 MB (6733368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530232ef45f9be28c51b27fb2731af7ada5b7f97d0f4a568f10d1e49e47fce76`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d6068231fa01cd034e572c03b44e1a8604fc46e1192d6fc7c315969afbc96`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2907e86db3b43ad365ed9c4d0cc9edb1061ae9ac1b25cd8a9f780760f60f92`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 49.6 MB (49594160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32227a5f90ca9af772fed7924537628d1269c2e6314c0d94d7004a0b6d4dc`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a236ad6589381808c63af9eb734df49b71b51701ca9cda9a14b5a26a8f3c36`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 64.0 MB (64005067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c5c9ac9cf8df20da0c839b9d2d288896c1ddefe9481d57de2804f89df3165`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05654ed9c1054be2de70cb56a24b6596e4f988350906304c4023ba10b17c3b9f`  
		Last Modified: Wed, 16 Oct 2024 16:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:f5e5de72449e78e87d38a283907a9d5730a3333b140f1f909bef338d53519b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a617ceb17c6bb429c78f168af71aa1444c3c5a59c581e694ea1baa6bca0f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6a311f8b51d12c3849c0407654cf4db852229667956b1cbbfa786c1d71629607`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 14.7 MB (14749144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad722472f637e5a13b51d32491bc581ab6fc14b00652932d6a817124967a86c4`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 35.0 KB (34955 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:bf79508626d6cad5bd82ea762109690e42467b1eefedab27946eccd69ab23069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1c9a74f109e3f0652a74e26835d483cf43412611a0c9895e03ee6694a6703698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170572138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d6b00bceda8e96d5a84590808ba2cb6dca6c020971ed438e50ac3af798c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6111251d1d05a298b2e671590545d81d77f605a0909a7a78131c0639d1aa6dd7`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669648c0f2f15956edcf8b8789c3603322ef63cb3bb77d558add2b4848858bf`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19c425e6ff82725f7cce8c81138dad656b6efff512313e3b80402fb9da218d`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 6.7 MB (6733368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530232ef45f9be28c51b27fb2731af7ada5b7f97d0f4a568f10d1e49e47fce76`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d6068231fa01cd034e572c03b44e1a8604fc46e1192d6fc7c315969afbc96`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2907e86db3b43ad365ed9c4d0cc9edb1061ae9ac1b25cd8a9f780760f60f92`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 49.6 MB (49594160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32227a5f90ca9af772fed7924537628d1269c2e6314c0d94d7004a0b6d4dc`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a236ad6589381808c63af9eb734df49b71b51701ca9cda9a14b5a26a8f3c36`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 64.0 MB (64005067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c5c9ac9cf8df20da0c839b9d2d288896c1ddefe9481d57de2804f89df3165`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05654ed9c1054be2de70cb56a24b6596e4f988350906304c4023ba10b17c3b9f`  
		Last Modified: Wed, 16 Oct 2024 16:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f5e5de72449e78e87d38a283907a9d5730a3333b140f1f909bef338d53519b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a617ceb17c6bb429c78f168af71aa1444c3c5a59c581e694ea1baa6bca0f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6a311f8b51d12c3849c0407654cf4db852229667956b1cbbfa786c1d71629607`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 14.7 MB (14749144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad722472f637e5a13b51d32491bc581ab6fc14b00652932d6a817124967a86c4`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 35.0 KB (34955 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:bf79508626d6cad5bd82ea762109690e42467b1eefedab27946eccd69ab23069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1c9a74f109e3f0652a74e26835d483cf43412611a0c9895e03ee6694a6703698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170572138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d6b00bceda8e96d5a84590808ba2cb6dca6c020971ed438e50ac3af798c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6111251d1d05a298b2e671590545d81d77f605a0909a7a78131c0639d1aa6dd7`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669648c0f2f15956edcf8b8789c3603322ef63cb3bb77d558add2b4848858bf`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19c425e6ff82725f7cce8c81138dad656b6efff512313e3b80402fb9da218d`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 6.7 MB (6733368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530232ef45f9be28c51b27fb2731af7ada5b7f97d0f4a568f10d1e49e47fce76`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d6068231fa01cd034e572c03b44e1a8604fc46e1192d6fc7c315969afbc96`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2907e86db3b43ad365ed9c4d0cc9edb1061ae9ac1b25cd8a9f780760f60f92`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 49.6 MB (49594160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32227a5f90ca9af772fed7924537628d1269c2e6314c0d94d7004a0b6d4dc`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a236ad6589381808c63af9eb734df49b71b51701ca9cda9a14b5a26a8f3c36`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 64.0 MB (64005067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c5c9ac9cf8df20da0c839b9d2d288896c1ddefe9481d57de2804f89df3165`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05654ed9c1054be2de70cb56a24b6596e4f988350906304c4023ba10b17c3b9f`  
		Last Modified: Wed, 16 Oct 2024 16:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f5e5de72449e78e87d38a283907a9d5730a3333b140f1f909bef338d53519b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a617ceb17c6bb429c78f168af71aa1444c3c5a59c581e694ea1baa6bca0f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6a311f8b51d12c3849c0407654cf4db852229667956b1cbbfa786c1d71629607`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 14.7 MB (14749144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad722472f637e5a13b51d32491bc581ab6fc14b00652932d6a817124967a86c4`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 35.0 KB (34955 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40`

```console
$ docker pull mysql@sha256:bf79508626d6cad5bd82ea762109690e42467b1eefedab27946eccd69ab23069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40` - linux; amd64

```console
$ docker pull mysql@sha256:1c9a74f109e3f0652a74e26835d483cf43412611a0c9895e03ee6694a6703698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170572138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d6b00bceda8e96d5a84590808ba2cb6dca6c020971ed438e50ac3af798c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6111251d1d05a298b2e671590545d81d77f605a0909a7a78131c0639d1aa6dd7`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669648c0f2f15956edcf8b8789c3603322ef63cb3bb77d558add2b4848858bf`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19c425e6ff82725f7cce8c81138dad656b6efff512313e3b80402fb9da218d`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 6.7 MB (6733368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530232ef45f9be28c51b27fb2731af7ada5b7f97d0f4a568f10d1e49e47fce76`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d6068231fa01cd034e572c03b44e1a8604fc46e1192d6fc7c315969afbc96`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2907e86db3b43ad365ed9c4d0cc9edb1061ae9ac1b25cd8a9f780760f60f92`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 49.6 MB (49594160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32227a5f90ca9af772fed7924537628d1269c2e6314c0d94d7004a0b6d4dc`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a236ad6589381808c63af9eb734df49b71b51701ca9cda9a14b5a26a8f3c36`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 64.0 MB (64005067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c5c9ac9cf8df20da0c839b9d2d288896c1ddefe9481d57de2804f89df3165`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05654ed9c1054be2de70cb56a24b6596e4f988350906304c4023ba10b17c3b9f`  
		Last Modified: Wed, 16 Oct 2024 16:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:f5e5de72449e78e87d38a283907a9d5730a3333b140f1f909bef338d53519b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a617ceb17c6bb429c78f168af71aa1444c3c5a59c581e694ea1baa6bca0f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6a311f8b51d12c3849c0407654cf4db852229667956b1cbbfa786c1d71629607`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 14.7 MB (14749144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad722472f637e5a13b51d32491bc581ab6fc14b00652932d6a817124967a86c4`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 35.0 KB (34955 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-bookworm`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-debian`

```console
$ docker pull mysql@sha256:49b84fc5916192e766f6879127d4d871e7101e73bd15ca63df4c1d5ba6d08946
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.40-debian` - linux; amd64

```console
$ docker pull mysql@sha256:3e02ef51dfc79b03db86b7c0062d3bad3fd9f0387e2fa840842e7ef9d88d8e2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.2 MB (184176649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f1a2fa05087a2bce3781e5a57e32d535725a128a9aaf69b011d956b6face15`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Mon, 14 Oct 2024 22:15:13 GMT
ADD file:90b9dd8f12120e8b2cd3ece45fcbe8af67e40565e2032a40f64bd921c43e2ce7 in / 
# Mon, 14 Oct 2024 22:15:13 GMT
CMD ["bash"]
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
	-	`sha256:a480a496ba95a197d587aa1d9e0f545ca7dbd40495a4715342228db62b67c4ba`  
		Last Modified: Thu, 17 Oct 2024 00:23:58 GMT  
		Size: 29.1 MB (29126289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2811da9b019eed58703a8ada1caa82533276039c52ab3a74636da84859bb40`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2baf8dba5bbe9c68e00b53d352e48e4318bcc4a3c0ea7fe20dec9e8e87ff76d`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.4 MB (4422704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a614d15f9c06d6e6a1a248d99e306b85add43031f83f974b2c2022d053e71d9c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 1.4 MB (1445878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726b0c5e04163f0547e7229170628d079ee2f838019b64fefc9340f72fe61981`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f22d133288ad4b83b330050601bd2eb187e6768ea330fc18eb963a1304fa8d`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 15.3 MB (15294765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620060781f1e82b4ac6bad00e2e313caaab1042776b930c56738c1a226f76e67`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69095101e4f64ba06332cc8edb2fff22d36813c27f809a8bd66d4825cf3a8316`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47961d443cea8428d3cd3f6ccbf24fd7a9e48b723b8618f8f18f6206623dc2a6`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 133.9 MB (133876747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15871d93458f7e05360fc45c0b2a69b059a68f66b3cbc5aeca7e17d7707fa3ee`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82da9494c1cfa82f7466d409529f09d1c38c9e30724b1afce7f1d6060a10f88f`  
		Last Modified: Thu, 17 Oct 2024 01:31:10 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ceddd40e6b584c3483837f8f5963dfefe3a13ee11afc33b4bb749f8ab92ae5`  
		Last Modified: Thu, 17 Oct 2024 01:31:11 GMT  
		Size: 121.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:2ca39339c819cf8ea1fdb2d6531b8993ebfa93cf849801e2cf0f3737571ccefe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (4015748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9790f7c41dfb8ef68d613e084aa436d073d249302dc3722d4b519ee8eca4fff`

```dockerfile
```

-	Layers:
	-	`sha256:cfc62b48f0159d49308ec5353528a4853d89d4807bdf056f3148e66ffc9fe38c`  
		Last Modified: Thu, 17 Oct 2024 01:31:09 GMT  
		Size: 4.0 MB (3981572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3239c31101b2d7721588207b13bda72001e4f00ffd0cdac796931dacca981f98`  
		Last Modified: Thu, 17 Oct 2024 01:31:08 GMT  
		Size: 34.2 KB (34176 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oracle`

```console
$ docker pull mysql@sha256:bf79508626d6cad5bd82ea762109690e42467b1eefedab27946eccd69ab23069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:1c9a74f109e3f0652a74e26835d483cf43412611a0c9895e03ee6694a6703698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170572138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d6b00bceda8e96d5a84590808ba2cb6dca6c020971ed438e50ac3af798c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6111251d1d05a298b2e671590545d81d77f605a0909a7a78131c0639d1aa6dd7`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669648c0f2f15956edcf8b8789c3603322ef63cb3bb77d558add2b4848858bf`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19c425e6ff82725f7cce8c81138dad656b6efff512313e3b80402fb9da218d`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 6.7 MB (6733368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530232ef45f9be28c51b27fb2731af7ada5b7f97d0f4a568f10d1e49e47fce76`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d6068231fa01cd034e572c03b44e1a8604fc46e1192d6fc7c315969afbc96`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2907e86db3b43ad365ed9c4d0cc9edb1061ae9ac1b25cd8a9f780760f60f92`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 49.6 MB (49594160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32227a5f90ca9af772fed7924537628d1269c2e6314c0d94d7004a0b6d4dc`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a236ad6589381808c63af9eb734df49b71b51701ca9cda9a14b5a26a8f3c36`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 64.0 MB (64005067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c5c9ac9cf8df20da0c839b9d2d288896c1ddefe9481d57de2804f89df3165`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05654ed9c1054be2de70cb56a24b6596e4f988350906304c4023ba10b17c3b9f`  
		Last Modified: Wed, 16 Oct 2024 16:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:f5e5de72449e78e87d38a283907a9d5730a3333b140f1f909bef338d53519b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a617ceb17c6bb429c78f168af71aa1444c3c5a59c581e694ea1baa6bca0f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6a311f8b51d12c3849c0407654cf4db852229667956b1cbbfa786c1d71629607`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 14.7 MB (14749144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad722472f637e5a13b51d32491bc581ab6fc14b00652932d6a817124967a86c4`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 35.0 KB (34955 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.40-oraclelinux9`

```console
$ docker pull mysql@sha256:bf79508626d6cad5bd82ea762109690e42467b1eefedab27946eccd69ab23069
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0.40-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:1c9a74f109e3f0652a74e26835d483cf43412611a0c9895e03ee6694a6703698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170572138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a8d6b00bceda8e96d5a84590808ba2cb6dca6c020971ed438e50ac3af798c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6111251d1d05a298b2e671590545d81d77f605a0909a7a78131c0639d1aa6dd7`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669648c0f2f15956edcf8b8789c3603322ef63cb3bb77d558add2b4848858bf`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f19c425e6ff82725f7cce8c81138dad656b6efff512313e3b80402fb9da218d`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 6.7 MB (6733368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530232ef45f9be28c51b27fb2731af7ada5b7f97d0f4a568f10d1e49e47fce76`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880d6068231fa01cd034e572c03b44e1a8604fc46e1192d6fc7c315969afbc96`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2907e86db3b43ad365ed9c4d0cc9edb1061ae9ac1b25cd8a9f780760f60f92`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 49.6 MB (49594160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea32227a5f90ca9af772fed7924537628d1269c2e6314c0d94d7004a0b6d4dc`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a236ad6589381808c63af9eb734df49b71b51701ca9cda9a14b5a26a8f3c36`  
		Last Modified: Wed, 16 Oct 2024 16:21:20 GMT  
		Size: 64.0 MB (64005067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c5c9ac9cf8df20da0c839b9d2d288896c1ddefe9481d57de2804f89df3165`  
		Last Modified: Wed, 16 Oct 2024 16:21:18 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05654ed9c1054be2de70cb56a24b6596e4f988350906304c4023ba10b17c3b9f`  
		Last Modified: Wed, 16 Oct 2024 16:21:19 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:f5e5de72449e78e87d38a283907a9d5730a3333b140f1f909bef338d53519b1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14784099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50a617ceb17c6bb429c78f168af71aa1444c3c5a59c581e694ea1baa6bca0f1d`

```dockerfile
```

-	Layers:
	-	`sha256:6a311f8b51d12c3849c0407654cf4db852229667956b1cbbfa786c1d71629607`  
		Last Modified: Wed, 16 Oct 2024 16:21:17 GMT  
		Size: 14.7 MB (14749144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad722472f637e5a13b51d32491bc581ab6fc14b00652932d6a817124967a86c4`  
		Last Modified: Wed, 16 Oct 2024 16:21:16 GMT  
		Size: 35.0 KB (34955 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0.40-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:6520dab1da3b1754c9d51e34141fc1d456d4956d1b0d1a42ab887f1d935ce2f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.1 MB (175149112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b1f811389973b63b5508f81cd1bceaf409f1d9ad51b87d6639b619db229cdc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2152ccfb177be7e51d0069975827ccecd99b035be6c006a029afc2bf6d2c94`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4855413356a2f85d8b1ee126d760d53d70170cf1aa368d983b55468bc5e169ea`  
		Last Modified: Wed, 16 Oct 2024 00:10:18 GMT  
		Size: 48.5 MB (48463357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050fccf8a3771f299aee6da5560f493cdee2f91c0bf2efbc77aaaeb5ce91fdf`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f86890bcfb7ebac225b5b70ffcda6c2e1aeb413c7b5bffb69a422c275c81d2`  
		Last Modified: Wed, 16 Oct 2024 00:10:19 GMT  
		Size: 71.5 MB (71517547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dde3d188397939717077a45ad9f1bc78b84e2bc2b769b96c4244449879f52c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad11f03a0bf4a8df5922056f7ef8bac558bde47ae6ab8dab1289b48cb4324469`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.40-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:1c805d1c6b89f40359762cff3c76fac32bac069b1fd50cbfd96f5a0c1b256126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14779425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cef5625b474ac43b3353e786497a0041ffd5a860601ebc1812481c8b82b27f5`

```dockerfile
```

-	Layers:
	-	`sha256:486349e6b6e6aa26a5c0adfce78101618e256e568f73bf9ce18715d0bb2daf6c`  
		Last Modified: Wed, 16 Oct 2024 00:10:17 GMT  
		Size: 14.7 MB (14744222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e18bf5414ab71c2aae4cda176f8b2909e0ebc923a7cdfa6baaf541173c134cc`  
		Last Modified: Wed, 16 Oct 2024 00:10:16 GMT  
		Size: 35.2 KB (35203 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oracle`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.3-oraclelinux9`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4.3-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4.3-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.3-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oracle`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1-oraclelinux9`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oracle`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.1.0-oraclelinux9`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:9.1.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:9.1.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.1.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:bda6ee1f3ae5ebb3cbe9b995c9645ffbd36d7dbda3bd4b4d2ffa43d997073074
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:779f2c470d1ee5c84ef7f5fb6514ed4c2ebf659697c8625bc2729be748abc69f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.1 MB (171126173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7aff0191ea53fafcae68c591ffaeaec6c2d47c34efa1e27d45c4d614b775f11`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b328be7f3cf1ba5c1f0f907adf6298562b2363f669c3fa65e7687cec812e0a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfccffffaa132f105d050bcd87d4abe023713c180e3cf5297ef86a4bc7f58cfe`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e0a5533d8eb7e141fb29b6cb9faa19ad285f9e44805036c5933b43e0c5bec6`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 6.7 MB (6733363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5394d74c14215a3d711d257b01cb30b1f5b483a3a95913a4ea8b23fcbd84760`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7dbd4762de4988eb769de8858ca997f02e48dbdf96a62b633c2e4ddb8dd70a`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d47438f1e4ce915600d70dc0c2922f2b855d5be03ff3442bc85fd3445e06e7`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 47.5 MB (47546230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403b4956745f3e435975e88e8e4c67ba4466a0339bb6608dab9ccdf5085e75a1`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf348cec4fb4a5dfae95f79049fa4d87f736bb115e7e1c1110a606a595e14c5`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 66.6 MB (66607158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44a5b7781d0f6268d6dc639e1fe7a3921401147f3244b522c3a5daee6e65af3`  
		Last Modified: Wed, 16 Oct 2024 16:20:35 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3ba5507b8d8f6327640cc3c3e8f2b6b3a5c47411790d7c5e5335a2e888ce7617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14890918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f10459874f83eb3f9b88ba1b5b1bcc0eef978b5940fd937e53e7fd8c2f98c6f`

```dockerfile
```

-	Layers:
	-	`sha256:b427a7694495e32b96bb48a6ca017a78c394832c86d0849f5c245183683bdd44`  
		Last Modified: Wed, 16 Oct 2024 16:20:34 GMT  
		Size: 14.9 MB (14856665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ea9aef7fd2178cc6e6dbc9419b9a0da1e3f61219a21d47d783e9f040aecebe2`  
		Last Modified: Wed, 16 Oct 2024 16:20:33 GMT  
		Size: 34.3 KB (34253 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:dd256091ee3999c09acb4ced7fb3f3b2a89b552df308722dd00b72f77c44cffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168408031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b15f39a8d08f52383c96251e6cadf7d1015c0cf77b75114f659cd8fb02139b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b7028800541ec5f9b572ea0a94c73bfc3c9a084ff6cf3c5dbdab907e579336`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 336.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3688c019d38ddb128748361bc8442855e57af0db88f0e93834031ce7244fb4`  
		Last Modified: Wed, 16 Oct 2024 00:08:51 GMT  
		Size: 46.4 MB (46434642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612ab3e6f2e455dba7f722ec39906cc89be259bbd798d556622d815bfad7a64e`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b399be0ddb3217783e7225debbe946872a9ea299a8be2339720bf23df71f402`  
		Last Modified: Wed, 16 Oct 2024 00:08:52 GMT  
		Size: 66.8 MB (66805294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8149d82fe4db2b12985770e814c59b72e0e4f741e0c7021a37b6974559050238`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:633e255e1c4079c4a93fd6ecb4347f80c971d45c588cb0ce0896514c23207ea3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14886373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:785ff7b653c6b06c14d111e7fe2a52fd7a4d77ce1b42864667a3d82a5e53bac0`

```dockerfile
```

-	Layers:
	-	`sha256:a9e72cd10253f726a570d12f99129d1109a3f5a7da0f777a2a7e8d03bd3ca990`  
		Last Modified: Wed, 16 Oct 2024 00:08:50 GMT  
		Size: 14.9 MB (14851815 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a10bb947e8eeb52a4cafe01070040e1a8fcd1347a70be1bcecc0509651ef83e`  
		Last Modified: Wed, 16 Oct 2024 00:08:49 GMT  
		Size: 34.6 KB (34558 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:fd8d1b4e287c49e1e35eb5a103f337111947662130eb8a3e6c3e823813f47f7d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:a8298c3d874784d92f5f34f279a6fbf92c6ba69628548bb380db29f2bca9dd18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.9 MB (173911893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be960704dfac8744a2e2df80c90087551a998ac008916b9d1423d7b0c5ee33ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:00 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:00 GMT
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
	-	`sha256:eba3c26198b76ce92acfa6308130ab3224ee9fff583c51487a8caa0336d59e4e`  
		Last Modified: Fri, 20 Sep 2024 17:57:55 GMT  
		Size: 49.2 MB (49246942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f7c8c33abe1138c12d45d7a453df15f348b13043bbdc1c5bbe95e07dfa6403`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa23d877fa04f2edd527357b3a38ac6199bfdc0e7b09b3b64f9424528a168e03`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 983.0 KB (983005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a143609ddd2d82d253ae60d2f6604cdc7df34ed671b0e24707c31a78800ee88c`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 6.7 MB (6733149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78308a3437c4e14b44bb662c504c2a8c1b2ef7142207787bea32157cc91e3fe9`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 2.6 KB (2610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0880e4b37373adae469fec17a9d0947481f0a105bd70a901556aaa66ff6f246`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bab267f9ce1d6b904aeec7a381caf991e717163fb9f56a67d347f9c1927bd2a`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 48.2 MB (48194482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e575f6d9b17aa2a17b5604b104d60f453cc7f7944980cb645be85bcf31805494`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607f86c00053926c764f5761ea2f19822ab243ed23cd1eff55b0d61deabb46d4`  
		Last Modified: Wed, 16 Oct 2024 16:19:56 GMT  
		Size: 68.7 MB (68744832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd68caa5febee3feb96495599d9f764927c0feed19ba48664a94ab33731351ca`  
		Last Modified: Wed, 16 Oct 2024 16:19:55 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:9f5233de23cafeaf8d75934a50668ba51dc0101a2e4cd0e54f4dc938fa472e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14896444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d448d7377f748f99f658cca996eb870f7ea3178c4b4f7a0c9d7531d9a65f622b`

```dockerfile
```

-	Layers:
	-	`sha256:e1acb92f5dbc9b0fda5a12ad4cd5a8262e541cd205891da03c53b99f7fd47286`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 14.9 MB (14861124 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d34fe5a41256c3c71d027bca29d1ab97717eceb94e81e9c41539a5b8f415219`  
		Last Modified: Wed, 16 Oct 2024 16:19:54 GMT  
		Size: 35.3 KB (35320 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:42a8303caf8f55c2d99e7db9955c1766f79ca94887655e3fc88554297abf4a01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.2 MB (171192378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22aaacaafc0e7ec1fe9dde21dcc39fd815cec2f4c58a07b2bbe25410fc223203`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 20 Sep 2024 15:14:52 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Fri, 20 Sep 2024 15:14:52 GMT
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
	-	`sha256:8b4274ea61c534aa5fa98d1b58b535c6b61e25446a34137658cf3b735bd6a02c`  
		Last Modified: Fri, 20 Sep 2024 17:59:19 GMT  
		Size: 47.9 MB (47914583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba006fa9b4bbf01f91fee6b0164d7a7855be0c5063bd7d2d214c0df88f3639`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 885.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a1aa4ee2ea7983a656589468342df8f65e19291af23086a0cd638ee01da493`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 913.5 KB (913454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df48654477e31713a1acfcc889611e846b3b2da966d25d62ffc29c559b6820a3`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 6.3 MB (6330580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bc7a62e19afac2019e0b152521a1c5ff2f9b888644fafafe5bcbe0c375e568`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 2.6 KB (2607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806ebf9b9401ab4417e21f49fde4840faf2237b281f98999eabbfffc2220e08f`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037f0555e71d3413d9cadffbea357382edbb8025379c9a53163efa6736b382c`  
		Last Modified: Wed, 16 Oct 2024 00:07:19 GMT  
		Size: 47.1 MB (47097988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace4982789bf0c155a1fd1728613944e52d2e6deea813a521dc0dd251ae92c`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ead6e17e269cfb672fdd99d74fc6f0fa909c969364eff00003bbac032ea508`  
		Last Modified: Wed, 16 Oct 2024 00:07:20 GMT  
		Size: 68.9 MB (68926288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d624aa804ccd589f71324347f8f8f99ab5c5fba1a1776d3a1a7841617c0d8e8d`  
		Last Modified: Wed, 16 Oct 2024 00:07:18 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:76e1eae8e7c36eeb22473bdf8dcaa817411f33e0de7b441069b397175e2dd49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14891971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18422a436c82fa5ba2964ea485cb8f4bed2a34b84205bdc5fdbad69c47efc68a`

```dockerfile
```

-	Layers:
	-	`sha256:57204ad646e254590d02be35b9fafc1c45e1885b847641dbbb870b94f62a11e7`  
		Last Modified: Wed, 16 Oct 2024 00:07:17 GMT  
		Size: 14.9 MB (14856310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd54905b85b07e4b9401dd8be47586855f124cee4fa6bdf4711fcb465e520b6d`  
		Last Modified: Wed, 16 Oct 2024 00:07:16 GMT  
		Size: 35.7 KB (35661 bytes)  
		MIME: application/vnd.in-toto+json
