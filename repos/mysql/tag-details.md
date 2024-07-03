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
-	[`mysql:8.0.38`](#mysql8038)
-	[`mysql:8.0.38-bookworm`](#mysql8038-bookworm)
-	[`mysql:8.0.38-debian`](#mysql8038-debian)
-	[`mysql:8.0.38-oracle`](#mysql8038-oracle)
-	[`mysql:8.0.38-oraclelinux9`](#mysql8038-oraclelinux9)
-	[`mysql:8.4`](#mysql84)
-	[`mysql:8.4-oracle`](#mysql84-oracle)
-	[`mysql:8.4-oraclelinux9`](#mysql84-oraclelinux9)
-	[`mysql:8.4.1`](#mysql841)
-	[`mysql:8.4.1-oracle`](#mysql841-oracle)
-	[`mysql:8.4.1-oraclelinux9`](#mysql841-oraclelinux9)
-	[`mysql:9`](#mysql9)
-	[`mysql:9-oracle`](#mysql9-oracle)
-	[`mysql:9-oraclelinux9`](#mysql9-oraclelinux9)
-	[`mysql:9.0`](#mysql90)
-	[`mysql:9.0-oracle`](#mysql90-oracle)
-	[`mysql:9.0-oraclelinux9`](#mysql90-oraclelinux9)
-	[`mysql:9.0.0`](#mysql900)
-	[`mysql:9.0.0-oracle`](#mysql900-oracle)
-	[`mysql:9.0.0-oraclelinux9`](#mysql900-oraclelinux9)
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
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oracle`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8-oraclelinux9`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0`

```console
$ docker pull mysql@sha256:598bf8b783dddc9070e9011aeb1eb5947f0bf7c4eda8ac510906556b8a2b6d0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:2c1f9c922cd68f65ce86487a180802ee25568072f6a620689f780ebc9e2696d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8279f68ee77d5307715b9d4a14f48d937d98c75d847c55fb711f1fd905815f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991eb3c93d635a35f6bf96f275415b6fb3d49c5c61d8b235531b74eb51d37c1`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee250fe5d1f79dc5ee21f5a4be00dd2f2433a202d912e7471d3b278ef152acc2`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333fe8b06fc6fe748214ba95d2cbb9338aa3c61100250bdcd1e001256d5ee80`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 6.7 MB (6711692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b576bcdc3484ead5fe9c2acba2aee4f0c39c34a9b6a5e97ff7d1a3ffbea98`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e573b6b099a044627a2fa2475e38585645e81b7258f0983baaeea4c24a166`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2797560be722164012bd10d07cd4d1509a148a6213d36809b567da9ae6245cd5`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 49.1 MB (49147390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab8feae9ffd1b728300ec92e8286e3bde18d6d35f65991d5ea4ac0180280d3`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68d02817e289a0c6d6be0623df2895b48c19ff77f856e5ceb8689ddf81ba459`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 60.2 MB (60171903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2c5b495768029186c8f9b422c16151df5cbf5c018f09f6e6e1178dff76c602`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903730759b438ee82e11b38cd327890ba63b6e73eb1fbb308e04ed70867e32ac`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:14c3fb503548f653b40f4115634adb407711b049a9682ba152d98fb9612193b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf74ba2b3234436b3a5b9e2c8be8556f2fc0ccaf20dcde3844cb2c2a98a653eb`

```dockerfile
```

-	Layers:
	-	`sha256:e5a23bce621ef830d2b9e6523cdb7f268d37e99ffdb1d2885c0aa494c8b53439`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 13.4 MB (13448982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5236ef1010564fd7b377e35a2184e7ec79906fe0246d9a2182fd8e207e6922`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:46c567f030a7da42b5e56f46269f0e087064d9168a41de74feaaafe54f1dca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74886cb940293243a3df296211569f68640e47bbbfb7146d440953788ad061e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc4f805ee7a7fdd1bbe8e4259a240df90d51dd379fecf0379b5aa0ed8f9f1e`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a499fd6c5d0fcf36f4643dbfcb2964df7e9752b06985b6a132df038ef3adb17`  
		Last Modified: Fri, 21 Jun 2024 20:54:39 GMT  
		Size: 48.0 MB (48027996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5190b5e2a11f8a2422b944e8e1a60f804c425dff784f275e3fd0f109aea89404`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002aaa2879929ca55cbbcf097ccd507ac8097a7f2fca71fb31f19d0ea2301e55`  
		Last Modified: Fri, 21 Jun 2024 20:54:39 GMT  
		Size: 67.7 MB (67652170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1fe4de914262c3ee5c71e7b143dbe32c9ff696cba6464a3d28f92121fdd2cf`  
		Last Modified: Fri, 21 Jun 2024 20:54:38 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d42313aaf377fc541b23c07cce2792aa3c2b23194aa6d1ee2949de7bcee9ebd`  
		Last Modified: Fri, 21 Jun 2024 20:54:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:3a4d08c0b74eb8041faa1527b71290134c7f7f15094400660b110157b796de28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cec093cab833a39b29116d83a2e466584875f94b9df1ae16f63be4e3f798693`

```dockerfile
```

-	Layers:
	-	`sha256:b26dd44328fdd11df674a40e68eae586193f83c285bda943161160b48ab64e77`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 13.4 MB (13444201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e82e197f313a1af02fc3a0bfb90bf4fd76b2abab2a0126a92a2961df2381423`  
		Last Modified: Fri, 21 Jun 2024 20:54:36 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-bookworm`

```console
$ docker pull mysql@sha256:bad55a5bb69d6710927792384b5eb55669ee15dc85dca1888874e4a7993eecd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:191058e8f145d2d8794ca2ef7686f8df89f8beef0ecf772c80607886aa7f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184741219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa43e731b20b482d1b844248f22a4bec0b2783176715d890cd18a114a3444b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 18 Jun 2024 16:01:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b12af5b557c06c3a5c6dd975dd3686381c91b8ef931d9ab05a86fdb255d61`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88e593e6b408dd358d9a445e1084f70ec1eabdba282702cea7a6b942c0bbbe`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.4 MB (4422804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812b991e80fec0287ed574a1991a2d8c777b671d63b5daf22e191efc9f15637`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.4 MB (1449139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566764f5c2d992f68294268ee93f0ab724bfa4b7dd3d01e53bef6aeb80bf8a3c`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b68b73b8170fa31433ea9ffa40b6b50e51f8c0b1dd82a00d1a93061743291`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 15.3 MB (15281665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eabfac9e79d96e7bec68c3b0ff222212936c118f6992c53345c0ccfcad871f`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993ed90740c0149e5ee20f29c4509d21f3628e496e270b0c1dedf62e2fccbbf`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3521799e2bce5b1df28dce6c04c8212066e04cd24148030f5568726465661`  
		Last Modified: Wed, 19 Jun 2024 02:00:48 GMT  
		Size: 134.4 MB (134426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d31927a647d17f4cf62c30839e677c2ff7ef21ff57e78d6999a9eb4e6a24b`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bc340fbe849fdcd94680e6eb30ef7e3e9fd9b701d397599077f69931ca842`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a7068ba10db291aafa1814f51be521a8fc34037d95042a735378ce83cede9`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:03f4bf9b3949c0fe742c3b95751c0df37198b9abfbcabeb7973938387adc0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0520f607f6eb045b5246b556615b8b3ba7c196cccd7fd4f71d9365576e59260`

```dockerfile
```

-	Layers:
	-	`sha256:560a5de877f65c7f953932a45c5a0fe9f19f459b651ca47a96359df81dc3fc8d`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.0 MB (3953560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a7edf9cd73f114c4dc6e53229a73fdd6b05057ce33e996a1f9c9cac2a6e1c`  
		Last Modified: Wed, 19 Jun 2024 02:00:44 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:bad55a5bb69d6710927792384b5eb55669ee15dc85dca1888874e4a7993eecd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:191058e8f145d2d8794ca2ef7686f8df89f8beef0ecf772c80607886aa7f90c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184741219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa43e731b20b482d1b844248f22a4bec0b2783176715d890cd18a114a3444b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1debian12
# Tue, 18 Jun 2024 16:01:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY config/ /etc/mysql/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:347b12af5b557c06c3a5c6dd975dd3686381c91b8ef931d9ab05a86fdb255d61`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.1 KB (1106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88e593e6b408dd358d9a445e1084f70ec1eabdba282702cea7a6b942c0bbbe`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.4 MB (4422804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0812b991e80fec0287ed574a1991a2d8c777b671d63b5daf22e191efc9f15637`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 1.4 MB (1449139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566764f5c2d992f68294268ee93f0ab724bfa4b7dd3d01e53bef6aeb80bf8a3c`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b68b73b8170fa31433ea9ffa40b6b50e51f8c0b1dd82a00d1a93061743291`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 15.3 MB (15281665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53eabfac9e79d96e7bec68c3b0ff222212936c118f6992c53345c0ccfcad871f`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 2.5 KB (2503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b993ed90740c0149e5ee20f29c4509d21f3628e496e270b0c1dedf62e2fccbbf`  
		Last Modified: Wed, 19 Jun 2024 02:00:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb3521799e2bce5b1df28dce6c04c8212066e04cd24148030f5568726465661`  
		Last Modified: Wed, 19 Jun 2024 02:00:48 GMT  
		Size: 134.4 MB (134426903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26d31927a647d17f4cf62c30839e677c2ff7ef21ff57e78d6999a9eb4e6a24b`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9bc340fbe849fdcd94680e6eb30ef7e3e9fd9b701d397599077f69931ca842`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a7068ba10db291aafa1814f51be521a8fc34037d95042a735378ce83cede9`  
		Last Modified: Wed, 19 Jun 2024 02:00:47 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:03f4bf9b3949c0fe742c3b95751c0df37198b9abfbcabeb7973938387adc0705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0520f607f6eb045b5246b556615b8b3ba7c196cccd7fd4f71d9365576e59260`

```dockerfile
```

-	Layers:
	-	`sha256:560a5de877f65c7f953932a45c5a0fe9f19f459b651ca47a96359df81dc3fc8d`  
		Last Modified: Wed, 19 Jun 2024 02:00:45 GMT  
		Size: 4.0 MB (3953560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f6a7edf9cd73f114c4dc6e53229a73fdd6b05057ce33e996a1f9c9cac2a6e1c`  
		Last Modified: Wed, 19 Jun 2024 02:00:44 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:598bf8b783dddc9070e9011aeb1eb5947f0bf7c4eda8ac510906556b8a2b6d0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:2c1f9c922cd68f65ce86487a180802ee25568072f6a620689f780ebc9e2696d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8279f68ee77d5307715b9d4a14f48d937d98c75d847c55fb711f1fd905815f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991eb3c93d635a35f6bf96f275415b6fb3d49c5c61d8b235531b74eb51d37c1`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee250fe5d1f79dc5ee21f5a4be00dd2f2433a202d912e7471d3b278ef152acc2`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333fe8b06fc6fe748214ba95d2cbb9338aa3c61100250bdcd1e001256d5ee80`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 6.7 MB (6711692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b576bcdc3484ead5fe9c2acba2aee4f0c39c34a9b6a5e97ff7d1a3ffbea98`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e573b6b099a044627a2fa2475e38585645e81b7258f0983baaeea4c24a166`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2797560be722164012bd10d07cd4d1509a148a6213d36809b567da9ae6245cd5`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 49.1 MB (49147390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab8feae9ffd1b728300ec92e8286e3bde18d6d35f65991d5ea4ac0180280d3`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68d02817e289a0c6d6be0623df2895b48c19ff77f856e5ceb8689ddf81ba459`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 60.2 MB (60171903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2c5b495768029186c8f9b422c16151df5cbf5c018f09f6e6e1178dff76c602`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903730759b438ee82e11b38cd327890ba63b6e73eb1fbb308e04ed70867e32ac`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:14c3fb503548f653b40f4115634adb407711b049a9682ba152d98fb9612193b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf74ba2b3234436b3a5b9e2c8be8556f2fc0ccaf20dcde3844cb2c2a98a653eb`

```dockerfile
```

-	Layers:
	-	`sha256:e5a23bce621ef830d2b9e6523cdb7f268d37e99ffdb1d2885c0aa494c8b53439`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 13.4 MB (13448982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5236ef1010564fd7b377e35a2184e7ec79906fe0246d9a2182fd8e207e6922`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:46c567f030a7da42b5e56f46269f0e087064d9168a41de74feaaafe54f1dca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74886cb940293243a3df296211569f68640e47bbbfb7146d440953788ad061e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc4f805ee7a7fdd1bbe8e4259a240df90d51dd379fecf0379b5aa0ed8f9f1e`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a499fd6c5d0fcf36f4643dbfcb2964df7e9752b06985b6a132df038ef3adb17`  
		Last Modified: Fri, 21 Jun 2024 20:54:39 GMT  
		Size: 48.0 MB (48027996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5190b5e2a11f8a2422b944e8e1a60f804c425dff784f275e3fd0f109aea89404`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002aaa2879929ca55cbbcf097ccd507ac8097a7f2fca71fb31f19d0ea2301e55`  
		Last Modified: Fri, 21 Jun 2024 20:54:39 GMT  
		Size: 67.7 MB (67652170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1fe4de914262c3ee5c71e7b143dbe32c9ff696cba6464a3d28f92121fdd2cf`  
		Last Modified: Fri, 21 Jun 2024 20:54:38 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d42313aaf377fc541b23c07cce2792aa3c2b23194aa6d1ee2949de7bcee9ebd`  
		Last Modified: Fri, 21 Jun 2024 20:54:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:3a4d08c0b74eb8041faa1527b71290134c7f7f15094400660b110157b796de28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cec093cab833a39b29116d83a2e466584875f94b9df1ae16f63be4e3f798693`

```dockerfile
```

-	Layers:
	-	`sha256:b26dd44328fdd11df674a40e68eae586193f83c285bda943161160b48ab64e77`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 13.4 MB (13444201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e82e197f313a1af02fc3a0bfb90bf4fd76b2abab2a0126a92a2961df2381423`  
		Last Modified: Fri, 21 Jun 2024 20:54:36 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oraclelinux9`

```console
$ docker pull mysql@sha256:598bf8b783dddc9070e9011aeb1eb5947f0bf7c4eda8ac510906556b8a2b6d0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:2c1f9c922cd68f65ce86487a180802ee25568072f6a620689f780ebc9e2696d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.0 MB (166017230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8279f68ee77d5307715b9d4a14f48d937d98c75d847c55fb711f1fd905815f16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0991eb3c93d635a35f6bf96f275415b6fb3d49c5c61d8b235531b74eb51d37c1`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 881.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee250fe5d1f79dc5ee21f5a4be00dd2f2433a202d912e7471d3b278ef152acc2`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0333fe8b06fc6fe748214ba95d2cbb9338aa3c61100250bdcd1e001256d5ee80`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 6.7 MB (6711692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37b576bcdc3484ead5fe9c2acba2aee4f0c39c34a9b6a5e97ff7d1a3ffbea98`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5e573b6b099a044627a2fa2475e38585645e81b7258f0983baaeea4c24a166`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2797560be722164012bd10d07cd4d1509a148a6213d36809b567da9ae6245cd5`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 49.1 MB (49147390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bab8feae9ffd1b728300ec92e8286e3bde18d6d35f65991d5ea4ac0180280d3`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c68d02817e289a0c6d6be0623df2895b48c19ff77f856e5ceb8689ddf81ba459`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 60.2 MB (60171903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac2c5b495768029186c8f9b422c16151df5cbf5c018f09f6e6e1178dff76c602`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903730759b438ee82e11b38cd327890ba63b6e73eb1fbb308e04ed70867e32ac`  
		Last Modified: Fri, 21 Jun 2024 20:51:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:14c3fb503548f653b40f4115634adb407711b049a9682ba152d98fb9612193b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13483763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf74ba2b3234436b3a5b9e2c8be8556f2fc0ccaf20dcde3844cb2c2a98a653eb`

```dockerfile
```

-	Layers:
	-	`sha256:e5a23bce621ef830d2b9e6523cdb7f268d37e99ffdb1d2885c0aa494c8b53439`  
		Last Modified: Fri, 21 Jun 2024 20:51:45 GMT  
		Size: 13.4 MB (13448982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d5236ef1010564fd7b377e35a2184e7ec79906fe0246d9a2182fd8e207e6922`  
		Last Modified: Fri, 21 Jun 2024 20:51:44 GMT  
		Size: 34.8 KB (34781 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.0-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:46c567f030a7da42b5e56f46269f0e087064d9168a41de74feaaafe54f1dca71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170570722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74886cb940293243a3df296211569f68640e47bbbfb7146d440953788ad061e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.0-server-minimal]'; 		echo 'name=MySQL 8.0 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.0-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.0.37-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bc4f805ee7a7fdd1bbe8e4259a240df90d51dd379fecf0379b5aa0ed8f9f1e`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a499fd6c5d0fcf36f4643dbfcb2964df7e9752b06985b6a132df038ef3adb17`  
		Last Modified: Fri, 21 Jun 2024 20:54:39 GMT  
		Size: 48.0 MB (48027996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5190b5e2a11f8a2422b944e8e1a60f804c425dff784f275e3fd0f109aea89404`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002aaa2879929ca55cbbcf097ccd507ac8097a7f2fca71fb31f19d0ea2301e55`  
		Last Modified: Fri, 21 Jun 2024 20:54:39 GMT  
		Size: 67.7 MB (67652170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1fe4de914262c3ee5c71e7b143dbe32c9ff696cba6464a3d28f92121fdd2cf`  
		Last Modified: Fri, 21 Jun 2024 20:54:38 GMT  
		Size: 5.3 KB (5331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d42313aaf377fc541b23c07cce2792aa3c2b23194aa6d1ee2949de7bcee9ebd`  
		Last Modified: Fri, 21 Jun 2024 20:54:38 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:3a4d08c0b74eb8041faa1527b71290134c7f7f15094400660b110157b796de28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.5 MB (13479311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cec093cab833a39b29116d83a2e466584875f94b9df1ae16f63be4e3f798693`

```dockerfile
```

-	Layers:
	-	`sha256:b26dd44328fdd11df674a40e68eae586193f83c285bda943161160b48ab64e77`  
		Last Modified: Fri, 21 Jun 2024 20:54:37 GMT  
		Size: 13.4 MB (13444201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e82e197f313a1af02fc3a0bfb90bf4fd76b2abab2a0126a92a2961df2381423`  
		Last Modified: Fri, 21 Jun 2024 20:54:36 GMT  
		Size: 35.1 KB (35110 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.38-bookworm`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.38-debian`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.38-oracle`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.0.38-oraclelinux9`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.4`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oracle`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4-oraclelinux9`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:8.4-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.1`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.4.1-oracle`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:8.4.1-oraclelinux9`

```console
$ docker pull mysql@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `mysql:9`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oracle`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9-oraclelinux9`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oracle`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.0`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0.0` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.0-oracle`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:9.0.0-oraclelinux9`

```console
$ docker pull mysql@sha256:9826de7445a4354eda5fc7a0d62163702b1dec76e375e6d54a8d3ec0a70766db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:9.0.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:9.0.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oracle`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:innovation-oraclelinux9`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:innovation-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:innovation-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:innovation-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:latest`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:latest` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:latest` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oracle`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:lts-oraclelinux9`

```console
$ docker pull mysql@sha256:dab7049abafe3a0e12cbe5e49050cf149881c0cd9665c289e5808b9dad39c9e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:3e5649c69e6d75cf88fc6f8f39f877453faa4e5167b5e648007e45f54bb17f6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.7 MB (168695819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05247af918647d8d063d2e880cc65c1546a7d616cde1e6c6f5dab1ca091f6cf8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d40f69285f8d245c760117939a657c8c515fd3647ee4bcd02d1ae1f9e44eee`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 882.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e5412f594e276b4842677da64016e1525572e907be4adeea9d7a15a398ab17`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 983.0 KB (983003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e00a64de64e912c594441615962b78c4bb7da616cb789d2bede1dbcdba205f72`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 6.7 MB (6711620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd3d47ce6c0418367dc6333f348f9f21574078bc71c2353cd6c84fc183e889`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 2.6 KB (2606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18af3efb629d667b19893d834584a8fa7c764d136e314974f29deabf8c71411c`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3db9dfd86e61d950577b9259a237591129aaad8a9b3cdc6a95ebe0295bbe1f`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 47.2 MB (47215827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787130cbc394beeb765c33afb0f1a3b0f81cf23494df2fc9c03ad06aea4cde91`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d458a23614968ea81dc28ae0a5f1a105ade2526e5d697856cb4ee87e758a7d2e`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 64.8 MB (64782245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48f1878172cbfcc8731bc72eca2971b5c5b81a30faff287932c2a19621b1624`  
		Last Modified: Fri, 21 Jun 2024 20:51:38 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:2d8865c91641b46966221611a5dfb88f9740581ef8d589cbaccc913853d1cb34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13596775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef1a2d95e9ddd1ee949271d04ab4e1ec731e7ed6d21d869685eec52759e28fa8`

```dockerfile
```

-	Layers:
	-	`sha256:e99e8d1a48c8597dd978f536d5f37fb4f8721aca2c8736b303d2892d13c9f326`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 13.6 MB (13560851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e137dbf01d7e83decc2bafdeb0afe9105c72839316a8355161b9234cfb838d`  
		Last Modified: Fri, 21 Jun 2024 20:51:37 GMT  
		Size: 35.9 KB (35924 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:lts-oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oracle`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oracle` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oracle` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:oraclelinux9`

```console
$ docker pull mysql@sha256:b41316975c64a7394c4f385566180d5743c9818583473b18bd6d74c41fa00cb9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:06f007b0c104e4d89318ccbdb19d06daea8e9232dbcda58cb7ceb40709acf5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170266975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ebb0b19998d2c1b8bcbb8fc0f0e676dcc9a758b2fea940f8e6aa27b4c916cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db774776bbe86ff76f53bb39d3892625f62a3c58d683f24ccc729457da407569`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 883.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b850c913cabffe1ee5f101cdf994b59e519c42f9319956e79886e55f252320b`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d9d23107fdae4f44db4d51181b506f244f7a79f3f6a1525fa0ff72c7bafd11`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 6.7 MB (6711660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5123b24fccfd2028a26a359d77146a66449f0a34cf98c6c7a65e0a05b5e55e`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0467c26f4a85761103bc5c09c0016456065ee717fc22ef5275852b31eb0263`  
		Last Modified: Tue, 02 Jul 2024 22:07:14 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65dd49246d7bed40a31467d8b94ff692f78d396ec7e8b95aba3612935cece6f`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 47.7 MB (47703990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08151edac83eb3b9edd7d8e60d0591b24ea9d2d7ce1506247798c0bb65e5c808`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4cbb0e2b3a87f57016deda9355e7423896fa100c3401f9f20097a8e8b9007e`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 65.9 MB (65865182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c68f7d2e616555e20312eccd7155eb0fb32e36ddf93bc678a897884b6ce5a4`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 5.3 KB (5328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:016d45177b0c75aec0319e018aae6fe1e5310bcc19f541a5397491a6fe554812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13831133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58c4e9063801cc1089c11e6a30157db8b8d1cc78e6be7e83e299feafcc5e3c9`

```dockerfile
```

-	Layers:
	-	`sha256:375da37b434761255cda552b1a75d1e39c58779c5d1d4aebb6ee416f23817adf`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 13.8 MB (13795993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7dadcca4f6b79cbb64f12aaab757ad269c908196be9fe75cc9e518f4dc3099c`  
		Last Modified: Tue, 02 Jul 2024 22:07:13 GMT  
		Size: 35.1 KB (35140 bytes)  
		MIME: application/vnd.in-toto+json

### `mysql:oraclelinux9` - linux; arm64 variant v8

```console
$ docker pull mysql@sha256:81e9d95d528511718b81cb9c548e1b922976bf359ed1083782bdbbbccf9ad85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.9 MB (165935645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26af66f0ce61786c7c80a4c3df3fc82449ba62eb649d2a456841697910e1e988`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 18 Jun 2024 16:01:15 GMT
ADD file:5f8c504a11c97baf0a932b85c5b4c4a1fb9e5096916bdacb18d89518ddb36350 in / 
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	groupadd --system --gid 999 mysql; 	useradd --system --uid 999 --gid 999 --home-dir /var/lib/mysql --no-create-home mysql # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	arch="$(uname -m)"; 	case "$arch" in 		aarch64) gosuArch='arm64' ;; 		x86_64) gosuArch='amd64' ;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 	curl -fL -o /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch.asc"; 	curl -fL -o /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$gosuArch"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y 		bzip2 		gzip 		openssl 		xz 		zstd 		findutils 	; 	microdnf clean all # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export --armor "$key" > /etc/pki/rpm-gpg/RPM-GPG-KEY-mysql; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_MAJOR=8.4
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql8.4-server-minimal]'; 		echo 'name=MySQL 8.4 Server Minimal'; 		echo 'enabled=1'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-8.4-community/docker/el/9/$basearch/'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-minimal.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-community-server-minimal-$MYSQL_VERSION"; 	microdnf clean all; 	grep -F 'socket=/var/lib/mysql/mysql.sock' /etc/my.cnf; 	sed -i 's!^socket=.*!socket=/var/run/mysqld/mysqld.sock!' /etc/my.cnf; 	grep -F 'socket=/var/run/mysqld/mysqld.sock' /etc/my.cnf; 	{ echo '[client]'; echo 'socket=/var/run/mysqld/mysqld.sock'; } >> /etc/my.cnf; 		! grep -F '!includedir' /etc/my.cnf; 	{ echo; echo '!includedir /etc/mysql/conf.d/'; } >> /etc/my.cnf; 	mkdir -p /etc/mysql/conf.d; 	mkdir -p /var/lib/mysql /var/run/mysqld; 	chown mysql:mysql /var/lib/mysql /var/run/mysqld; 	chmod 1777 /var/lib/mysql /var/run/mysqld; 		mkdir /docker-entrypoint-initdb.d; 		mysqld --version; 	mysql --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eu; 	{ 		echo '[mysql-tools-community]'; 		echo 'name=MySQL Tools Community'; 		echo 'baseurl=https://repo.mysql.com/yum/mysql-tools-8.4-community/el/9/$basearch/'; 		echo 'enabled=1'; 		echo 'gpgcheck=1'; 		echo 'gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-mysql'; 		echo 'module_hotfixes=true'; 	} | tee /etc/yum.repos.d/mysql-community-tools.repo # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENV MYSQL_SHELL_VERSION=8.4.0-1.el9
# Tue, 18 Jun 2024 16:01:15 GMT
RUN set -eux; 	microdnf install -y "mysql-shell-$MYSQL_SHELL_VERSION"; 	microdnf clean all; 		mysqlsh --version # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 18 Jun 2024 16:01:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 16:01:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 16:01:15 GMT
EXPOSE map[3306/tcp:{} 33060/tcp:{}]
# Tue, 18 Jun 2024 16:01:15 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:60ea4dc82df43adc83e6f0a288a75a467c20924311a1fd143690657725c2ebff`  
		Last Modified: Fri, 21 Jun 2024 19:42:43 GMT  
		Size: 47.7 MB (47652766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeaac00f5df03f6f38bf7ecc4769b9a23e55056025a5851c1a4d5c4686a8b7d`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93611301cba5889c772d61260e8efc0c7c1c37a70e8e7db9efc2b2cf67010e53`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 913.4 KB (913439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687d48bd5eed486f834f2aeeb98c3b31c69632e804094345d8fce02a284c911`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 6.3 MB (6314755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbb8564b525ee1fc261327bbc1a7f748c6f0cfb4c5b57fab5ecab6c2221b850`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 2.6 KB (2608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc1bd0a565d7cf1e2dc7481c126af4bc99d8452795d57895c45de63bf2fe9f48`  
		Last Modified: Fri, 21 Jun 2024 20:53:12 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d3d3a6688431c46150da632ff0efc970557606cbb0a203fda8d9d19a20990`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 46.1 MB (46085104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ed4303a4e50950db106c0879157df3c728f33abce028195ffb1b6043fb7315`  
		Last Modified: Fri, 21 Jun 2024 20:53:13 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690ceac92fb0094b530371d299c5daab1c86ef2eb84a309bb82c1c503e72c0`  
		Last Modified: Fri, 21 Jun 2024 20:53:15 GMT  
		Size: 65.0 MB (64960102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126b0c16732837c2e605f427369b409489aee417adb922a9b505fc1e2f6d7367`  
		Last Modified: Fri, 21 Jun 2024 20:53:14 GMT  
		Size: 5.3 KB (5333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:96c74d9c944ec216dd0905796e8266e5eda94c473ef92203cac63cf9ac813690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 MB (13592614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c494850bc9fd62051a3865528b786eb10a05e07a7c67a5130389dbffd49a4d5`

```dockerfile
```

-	Layers:
	-	`sha256:3de42c8f2b5abf1f1286cb643a75df2bad4f4cd8d9b1ec11f1f6577283cc3c68`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 13.6 MB (13556214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e4242312b762224f545c08985e96af2caa198878729e7929714cc0e98c88f2c`  
		Last Modified: Fri, 21 Jun 2024 20:53:11 GMT  
		Size: 36.4 KB (36400 bytes)  
		MIME: application/vnd.in-toto+json
