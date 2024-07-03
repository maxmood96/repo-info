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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:38ee060b800b8ce1b7c788900c33894e8fd0b194b37bf8da8564eb32f61d15d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
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
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-debian`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0-debian` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0-oracle`

```console
$ docker pull mysql@sha256:38ee060b800b8ce1b7c788900c33894e8fd0b194b37bf8da8564eb32f61d15d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
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
$ docker pull mysql@sha256:38ee060b800b8ce1b7c788900c33894e8fd0b194b37bf8da8564eb32f61d15d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.0-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
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
$ docker pull mysql@sha256:7ad421a2b2cdea510f465387eb4901264f688a11e7887e71dd905d7c9c7b6f35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-bookworm`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38-bookworm` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-bookworm` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-debian`

```console
$ docker pull mysql@sha256:40a5048901e4ac52df4705f3d068a197e3252c7f3a07aa4ff760dea0b7810b91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38-debian` - linux; amd64

```console
$ docker pull mysql@sha256:277149d61700e1e7a52e789e5ab8175bb7514c3c105f64838947a078eb210459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.7 MB (184749981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071e7158f1deb8a52948edaac253c4700938e65c1d432c8fc5919c2585a8e6f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:02 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Tue, 02 Jul 2024 01:25:02 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 04:16:15 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV GOSU_VERSION=1.17
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		openssl 		perl 		xz-utils 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN set -eux; 	key='BCA4 3417 C3B4 85DD 128E C6D4 B7B3 B788 A8D3 785C'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	mkdir -p /etc/apt/keyrings; 	gpg --batch --export "$key" > /etc/apt/keyrings/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_MAJOR=8.0
# Tue, 02 Jul 2024 04:16:15 GMT
ENV MYSQL_VERSION=8.0.38-1debian12
# Tue, 02 Jul 2024 04:16:15 GMT
RUN echo 'deb [ signed-by=/etc/apt/keyrings/mysql.gpg ] http://repo.mysql.com/apt/debian/ bookworm mysql-8.0' > /etc/apt/sources.list.d/mysql.list # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql # buildkit
# Tue, 02 Jul 2024 04:16:15 GMT
VOLUME [/var/lib/mysql]
# Tue, 02 Jul 2024 04:16:15 GMT
COPY config/ /etc/mysql/ # buildkit
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d87d8cc62e79471921338186c102bfc086a0bb323bbe85666d56912c136d31`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858653ba8771e4e38af8b3a226f2af89b9f0d155a839617623c1b1383e756146`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 4.4 MB (4422788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30635b624ad4265e473591178998548af2743d7833aa65b4217b190303238dec`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 1.4 MB (1445983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8ce947603c49fe6198179002d5fbc998a9a3ff9f6963a368cf3f4285c4cbfb`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7bb5d8550b9d5ca4baa5e193e5cb1f7c6b8584bd526fb645c1a5e0b7b8618f`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 15.3 MB (15285632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb77d4509f49c03d099cfa3365fdb27ef72feb2c5944a7c3bd2da6bf4f4483f6`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 2.5 KB (2504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5ad7cf18a49b99e3cb9efde239b479be2f72933582725c13b4de653dff8814`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6cea0fb09878e58a37fa58b538e8e5b196cd97532da35ddf6c53cb9cfc70ab`  
		Last Modified: Tue, 02 Jul 2024 22:07:04 GMT  
		Size: 134.5 MB (134459032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708143208d38455d198cfe3b828a3ac6a91a945fefddac974647efe2f8445a38`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 844.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c6eeeab6f29d3e7d2a2e30d447d2613b04e16d4d5f62e7f53782aae23790`  
		Last Modified: Tue, 02 Jul 2024 22:07:02 GMT  
		Size: 5.3 KB (5325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f27d906ab25538099e974ee34f36dc7118dde92e384ecd1769b6f6b0641f4ff`  
		Last Modified: Tue, 02 Jul 2024 22:07:03 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-debian` - unknown; unknown

```console
$ docker pull mysql@sha256:ac19d52d4c386d2606f4e7df4f6ab771fb55b6ba05a12edb80e90e9b9baac285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3987727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10617f86be6eb99c37ef9a103bf02fa6ecdcaf9af17d8b7d9198e06d5dc2dd99`

```dockerfile
```

-	Layers:
	-	`sha256:3fe3769d09da70fd03a312ced99a92cf04eb86eb699320ef01cd61d5a69272ed`  
		Last Modified: Tue, 02 Jul 2024 22:07:01 GMT  
		Size: 4.0 MB (3953589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:495fa7bf91beb283de4b6abd14421b7587e614581f2926cb08bc1bdb0049a92b`  
		Last Modified: Tue, 02 Jul 2024 22:07:00 GMT  
		Size: 34.1 KB (34138 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-oracle`

```console
$ docker pull mysql@sha256:7ad421a2b2cdea510f465387eb4901264f688a11e7887e71dd905d7c9c7b6f35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.0.38-oraclelinux9`

```console
$ docker pull mysql@sha256:7ad421a2b2cdea510f465387eb4901264f688a11e7887e71dd905d7c9c7b6f35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.0.38-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:ee0750b9a0ccb057443e063667f77762a85ed6d73c3942c0f87d194a573bfa9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.8 MB (166780981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b60ddd8609dec9f15e93e8965c3feaef46605794f7bfe9b6c27f84606199286`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88027a233423a01ed95373e67a0acb0ee38604cfddd2f23c9a43b43dcbc20cd5`  
		Last Modified: Tue, 02 Jul 2024 22:07:15 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1737d53d9c9be978097974d132e894e2c13d0da9524f9579e1c5efd6456a8`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 983.0 KB (983001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75710d2b88bab13ffab001b78ec5a0f6154e8f673180137960833aa5e058857b`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 6.7 MB (6711657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c637d449af440090fc97bdb3e65e38662c4128077285cdd68754062b17e2d7e7`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150fb8042aeeeacfda47344af7c0925db033ca2bec9b07c005a2e99514503fdc`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe60e377ebb7bb20099e6d821e6428aba44df520d9a68bd812ed161eebc291a6`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 49.2 MB (49164215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe3df0f185462276da470708b88605455a83732e4947b2d2bf59ea6381c7b1e`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b6d96e365ca71d22f3daa5934a534766daee12d67c954bc46aa216e2d11a3a`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 60.9 MB (60918865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febb53cf8cb27088b2cb140434c326844a38ad670fc86dd843fb3a55bd30a377`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 5.3 KB (5329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfdadb4716d771cc0da1fa7ef109d7bf91b2afeea661035171789e17581be31`  
		Last Modified: Tue, 02 Jul 2024 22:07:17 GMT  
		Size: 122.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.0.38-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:90132f893e2e2c5b86420117f433e90417e891b3dd234dd38eed78c47b575bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.7 MB (13717139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f857ed564e595cead83b6845b966dfffbed30feac67c038db189845a1841d858`

```dockerfile
```

-	Layers:
	-	`sha256:a29eabd56d69d0c81123a2f6fd824aa804e475958e8c29b9d829342969042954`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 13.7 MB (13682359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9957af9e6d3ddc4831b88372a0032d41974fee52363d5129d0e5658d1e354d`  
		Last Modified: Tue, 02 Jul 2024 22:07:16 GMT  
		Size: 34.8 KB (34780 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4`

```console
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:8.4-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:110f75257f7f0e21dce89bd5c6fb42089bc869ffd3f9e62bcd930bd796200440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.4.1` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.1-oracle`

```console
$ docker pull mysql@sha256:110f75257f7f0e21dce89bd5c6fb42089bc869ffd3f9e62bcd930bd796200440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.4.1-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

## `mysql:8.4.1-oraclelinux9`

```console
$ docker pull mysql@sha256:110f75257f7f0e21dce89bd5c6fb42089bc869ffd3f9e62bcd930bd796200440
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `mysql:8.4.1-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:8.4.1-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
		MIME: application/vnd.in-toto+json

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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oracle` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oracle` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
$ docker pull mysql@sha256:0a4acc6d272909a42df161d30b95ef1880f0fa07e9119e76de43f4563459ec3c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `mysql:lts-oraclelinux9` - linux; amd64

```console
$ docker pull mysql@sha256:e24bd134ee2ed1538953b9d16f1bc4ecfd3a09af42728d2d780b930c61669610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.5 MB (169469317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:736ced9665e85315558c1ffca8df196a5be5a6a0252139024a9f2867453bcb4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Fri, 21 Jun 2024 20:20:26 GMT
ADD file:fb24d10eda688c8fb542e360efb59a2b1eb790f9751caa9ee895ea79b8071a8a in / 
# Fri, 21 Jun 2024 20:20:26 GMT
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
	-	`sha256:7af76bb365463b0fc983b7c6bd02cea07bb7596f6e889859ef462654cc0293b6`  
		Last Modified: Fri, 21 Jun 2024 20:21:47 GMT  
		Size: 49.0 MB (48993653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fcbbd95294983a3cf663b45871ab9f014a18db38b4f3b9be5129fcbb71374b`  
		Last Modified: Tue, 02 Jul 2024 22:07:22 GMT  
		Size: 884.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbdb6512ec50df4b8814399d00bdf36a88bb861528b96d53df9138f0a6b048d`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 983.0 KB (983008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde54dd677dca49bf32b505637efc07cb4f47a066a41a1c3cc3f4f615cbbf08`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 6.7 MB (6711712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c32d19d44fe0839e4b9e5eb36cff2ba19b2544bff8f539f4b9b31b02eed490`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 2.6 KB (2605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77457e95149b5a6a8148280a17dba7c1075515c450ac32e361788361242eae2`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f71f60365b1d0738167f261630b4d8b2163ce907acfefb19d07cda3b16fafc`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 47.2 MB (47237078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a657cda140ef7e98110bc2fccebda1c9d61d9e8780b957363a12b206c0b5dd`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 320.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fc47757fc5f9639e584dce701d7eab605ed1c9b627ee0d340d8f115c80a382`  
		Last Modified: Tue, 02 Jul 2024 22:07:25 GMT  
		Size: 65.5 MB (65534393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0035d4d93c34889a303b5f234bd83d8c0d1fd308c8ce606fe9e6789c56c69c13`  
		Last Modified: Tue, 02 Jul 2024 22:07:24 GMT  
		Size: 5.3 KB (5330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mysql:lts-oraclelinux9` - unknown; unknown

```console
$ docker pull mysql@sha256:01f4137eaf9416d590d70bf3053d8f890392900028a32a29c7e280a8abff5fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13826449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfe8778dfc92127fa6f97147061dce47ff840cb90437ce8dbe25c7a18c750f8`

```dockerfile
```

-	Layers:
	-	`sha256:6277ab3d6077e4e176430da1ae72b084574f68619e6e43ae39f2f035bfd8a026`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 13.8 MB (13792376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85414c477cbf7938345ffe432a48de6387775948ed40ff8745cf4ce5736e8a44`  
		Last Modified: Tue, 02 Jul 2024 22:07:23 GMT  
		Size: 34.1 KB (34073 bytes)  
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
